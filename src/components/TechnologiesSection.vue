<template>
  <section>
    <h1>Tecnologias</h1>
    <div class="technologies-container">
      <div class="card vue">
        <img src="@/assets/images/icons/techs/VUE.png" alt="VUE-logo">
        <h1>Vue</h1>
      </div>
      <div class="card html">
        <img src="@/assets/images/icons/techs/HTML.png" alt="HTML-logo">
        <h1>HTML</h1>
      </div>
      <div class="card css">
        <img src="@/assets/images/icons/techs/CSS.png" alt="CSS-logo">
        <h1>CSS</h1>
      </div>
      <div class="card js">
        <img src="@/assets/images/icons/techs/JS.png" alt="JS-logo">
        <h1>JS</h1>
      </div>
    </div>
  </section>
</template>

<script setup>

</script>

<style scoped>
  @import url("@/assets/fonts/fonts.css");
  
  h1 {
    color: white;
  }

  section {
    height: 300px;
    width: 100%;
    align-items: center;
    flex-direction: column;
    display: flex;
  }

  .technologies-container {
  margin: 28px;
  display: flex;
  flex-wrap: wrap; /* Permite quebra de linha */
  gap: 28px;
  justify-content: center; /* Centraliza os cards */
  color: white;
  height: 100%;
  width: 100%;
}

  .card {
    display: flex;
    flex-direction: column;
    align-items: center;
    padding: 16px;
    border: 1px solid;
    border-radius: 8px;
    flex: 1 1 200px; /* Cresce, encolhe, base mínima */
    max-width: 220px;
    box-sizing: border-box;
  }

  .card img {
    height: 52px;
    width: auto;
    margin: 20px 0;
  }

  .card h1 {
    margin: 0;
    font-size: 16px;
  }  
  .vue {
    border-color: #3FB682;
  }
  .html {
    border-color: #FE4E1C;
  }
  .css {
    border-color: #0074BE;
  }
  .js {
    border-color: #F8DC3E;
  }

  @media (max-width: 880px) {
    section {
      height: 100%;
    }

    .card {
      flex: 1 1 80px;
      max-width: 100px;
      padding: 8px;
      height: auto; /* <- aqui está o truque */
    }

    .card img {
      height: 32px;
      margin: 10px 0;
    }

    .card h1 {
      font-size: 12px;
    }
  }


</style>