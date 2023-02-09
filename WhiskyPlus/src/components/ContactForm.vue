<template>
  <form class="email-form">
    <h2>{{ message }}</h2>
    <div class="form-group">
      <label>Email address</label>
      <input
        type="email"
        class="form-control"
        required
        placeholder="Skriv din mail"
      />
    </div>
    <div class="form-group">
      <label>Namn</label>
      <input type="text" class="form-control" placeholder="Skriv ditt namn" />
    </div>
    <div class="form-check">
      <input v-model="checked" type="checkbox" class="form-check-input" />
      <label class="form-check-label">I Agree to <a href="#">terms and conditions</a></label>
    </div>
    <button type="submit" @click="onSubmit()" class="btn btn-secondary">
      Prenumerera
    </button>
  </form>
</template>
<script>
export default {
  data() {
    return {
      checked: true,
      message: "Prenumerera på vårt nyhetsbrev",
    };
  },
  methods: {
    onSubmit() {
      alert("Tack för att du prenumerat till vårt nyhetsbrev!");
    },
  },
};
</script>
<style>
.email-form {
  padding: 3rem;
  margin: 5rem;
  border-radius: 2rem;
  background-color: #fff;
}
h2 {
  font-family: "Oswald", sans serifs;
  margin-bottom: 2rem;
}
</style>
