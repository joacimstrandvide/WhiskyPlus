<script setup>
import { RouterLink, RouterView } from "vue-router";
</script>
<template>
  <nav class="navbar navbar-expand-lg navbar-dark bg-dark">
    <div class="container-fluid">
      <RouterLink class="navbar-brand" to="/">WhiskyExtra</RouterLink>
      <div class="collapse navbar-collapse" id="navbarNav">
        <ul class="navbar-nav">
          <li class="nav-item">
            <RouterLink class="nav-link" aria-current="page" to="/"
              >Hem</RouterLink
            >
          </li>
          <li class="nav-item">
            <RouterLink class="nav-link" to="/about">Om Oss</RouterLink>
          </li>
          <li class="nav-item">
            <img src="../assets/img/cart.svg" alt="Cart" width="32" />
          </li>
        </ul>
      </div>
    </div>
  </nav>
  <RouterView />
</template>
<style scoped>
@import url("https://fonts.googleapis.com/css2?family=Oswald:wght@300;400;500&display=swap");
.navbar {
  font-family: "Oswald", sans serifs;
  color: #fff;
}

.nav-item img {
  position: absolute;
  right: 5%;
}

.nav-link {
  transition: 0.5s;
}

.nav-link:hover {
  color: #cf7f1d;
}
</style>
