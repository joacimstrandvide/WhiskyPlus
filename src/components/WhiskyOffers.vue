<template>
  <div class="col">
    <div class="card" style="width: 16rem">
      <img :src="`${whisky.image}`" class="card-img-top" alt="Whisky" />
      <div class="card-body">
        <h5 class="card-title">{{ whisky.name }}</h5>
        <p class="card-text">
          {{ whisky.description }}
        </p>
        <p class="card-text price">${{ whisky.price }}</p>
        <h5 class="sale" v-show="sale">REA!</h5>
      </div>
      <ul class="list-group list-group-flush">
        <li class="list-group-item">
          <h5 class="inStock" v-if="inStock">Finns I lager!</h5>
          <h5 class="noStock" v-else>Ej I Lager</h5>
        </li>
        <li class="list-group-item">
          <h5 :class="{ empty: amount < 10 }">Mängd: {{ whisky.amount }}</h5>
        </li>
        <a href="#" @click="addCart()" class="btn btn-success"
          >Lägg I Kundvagn</a
        >
      </ul>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      sale: this.whisky.sale,
      inStock: this.whisky.inStock,
      amount: this.whisky.amount,
    };
  },
  methods: {
    addCart() {
      alert("Varan Är Tillagd I Kundvagnen");
    },
  },
  props: {
    whisky: {
      required: true,
      type: Object,
    },
  },
};
</script>
<style>
@import url("https://fonts.googleapis.com/css2?family=Oswald:wght@300;400;500&display=swap");

.price {
  font-weight: 700;
  font-size: 1.5rem;
  color: #000;
}
.card {
  margin-bottom: 3rem;
  font-family: "Oswald", sans serifs;
}

.sale {
  color: #fff;
  background-color: green;
  padding: 0.3rem;
  margin: auto;
  width: 6rem;
  border-radius: 1rem;
}

.inStock {
  color: green;
}

.noStock,
.empty {
  color: red;
}

.list-group-item {
  border: none;
}
</style>
