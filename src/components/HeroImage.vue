<template>
  <div id="wrapper-hero">
    <img src="@/assets/img/HeroImage.jpg" class="img-fluid" alt="Hero Image" />
    <div class="centered">
      <h1>WhiskyPlus</h1>
      <h2>Whisky sedan 1967</h2>
    </div>
  </div>
</template>
<style scoped>
#wrapper-hero {
  position: relative;
  text-align: center;
  overflow: hidden;
}

#wrapper-hero img {
  width: 100%;
  height: auto;
  display: block;
}

.centered {
  position: absolute;
  top: 25%;
  right: 15%;
  color: #fff;
  font-family: "Oswald", sans-serif;
}

@media screen and (max-width: 768px) {
  .centered {
    right: 10%;
    top: 30%;
  }

  .centered h1 {
    font-size: 2rem;
  }

  .centered h2 {
    font-size: 1.2rem;
  }
}

@media screen and (max-width: 480px) {
  .centered {
    right: 5%;
    top: 25%;
  }

  .centered h1 {
    font-size: 1.8rem;
  }

  .centered h2 {
    font-size: 1rem;
  }

  #wrapper-hero img {
    height: auto;
  }
}
</style>
<script></script>
