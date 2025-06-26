<template>
  <section>
    <h1>Tecnologias</h1>
    <div class="technologies-container">
      <div class="card vue">
        <img src="@/assets/images/icons/techs/VUE.png" alt="">
        <h1>Vue</h1>
      </div>
      <div class="card html">
        <img src="" alt="">
        <h1>HTML</h1>
      </div>
      <div class="card css">
        <img src="" alt="">
        <h1>CSS</h1>
      </div>
      <div class="card js">
        <img src="" alt="">
        <h1>JS</h1>
      </div>
    </div>
  </section>
</template>

<script setup>

</script>

<style scoped>
  @import url("@/assets/fonts/fonts.css");
  /*@import url("@/assets/fonts/Montserrat/stylesheet.css");*/
  h1 {
    align-self: center;
  }
  
  .technologies-container {
    height: 300px;
    margin: 28px;
    display: flex;
    gap: 28px;
    align-items: center;
    justify-items: center;
    color: white;
  }
  .card {
    height: 150px;
    width: 150px;
    background-color: brown;
  }
  .card img {
    height: 40px;
    width: 40px;
  }
  
</style>