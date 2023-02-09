<script setup>
import HeroImage from "../components/HeroImage.vue";
import WhiskyOffers from "../components/WhiskyOffers.vue";
import ContactForm from "../components/ContactForm.vue";
</script>

<template>
  <HeroImage />
  <h1 class="title">{{ popular }}</h1>
  <div id="offers">
    <div class="container text-center">
      <div class="row align-items-start">
        <whisky-offers
          v-for="whisky in whiskys"
          :key="whisky.id"
          :whisky="whisky"
        />
      </div>
    </div>
  </div>
  <ContactForm />
</template>
<script>
export default {
  data() {
    return {
      popular: "Våra mest populära drycker",
      whiskys: [],
    };
  },
  components: {
    "whisky-offers": WhiskyOffers,
  },
  mounted() {
    this.fetchData();
  },
  methods: {
    async fetchData() {
      const res = await fetch("whisky.json");
      const val = await res.json();
      this.whiskys = val;
    },
  },
};
</script>
<style scoped>
@import url("https://fonts.googleapis.com/css2?family=Oswald:wght@300;400;500&display=swap");

#offers {
  display: flex;
  justify-content: center;
  margin-top: 10vh;
  margin-bottom: 10vh;
}
.title,
h1 {
  display: flex;
  justify-content: center;
  margin-top: 10vh;
  font-family: "Oswald", sans serifs;
  color: #fff;
}
</style>
