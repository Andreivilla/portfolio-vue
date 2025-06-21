<template>
  <div id="carousel-perfil-container">
    <input type="radio" name="position" checked />
    <input type="radio" name="position" />

    <div id="carousel">
      <div class="item">
        <img src="../assets/images/perfil/perfil-pixel.png" alt="">
      </div>
      <div class="item">
        <img src="../assets/images/perfil/perfil.png" alt="">
      </div>
    </div>
  </div>
</template>


<script setup>

</script>

<style scoped>
  * {
    margin: 0;
    display: grid;
    grid-template-rows: 500px 100px;
    grid-template-columns: 1fr 30px 30px 1fr;
    align-items: center;
    justify-items: center;
  }

  #carousel {
    grid-row: 1 / 2;
    grid-column: 1 / 5;
    width: 50vw;
    height: 100%;
    display: flex;
    align-items: center;
    justify-content: center;
    overflow: hidden;
    transform-style: preserve-3d;
    perspective: 600px;
    --items: 2;
    --middle: 2;
    --position: 1;
    pointer-events: none;
  }

  img {
    margin: 0;
    padding: 0;
    width: 100%;
    height: 100%;
    object-fit: contain;
    align-self: center;
  }

  .item {
    position: absolute;
    width: 300px;
    height: 400px;
    
    padding: 0;

    background-color: coral;  
    /*adicionar aqui um opacity algo assim
    e mudar a cor */

    --r: calc(var(--position) - var(--offset));
    --abs: max(calc(var(--r) * -1), var(--r));
    transition: all 0.25s linear;
    
    transform: rotateY(calc(-10deg * var(--r))) translateX(calc(-300px * var(--r)));
    
    opacity: calc(1 - (0.4 * var(--abs)));
    z-index: calc(10 - var(--abs));

    display: flex;
  }

  .item:nth-of-type(1) {
    --offset: 1;    
  }
  .item:nth-of-type(2) {
    --offset: 2;    
  }

  input:nth-of-type(1) {
    grid-column: 2 / 3;
    grid-row: 2 / 3;
  }
  input:nth-of-type(1):checked ~ #carousel {
    --position: 1;
  }

  input:nth-of-type(2) {
    grid-column: 3 / 4;
    grid-row: 2 / 3;
  }
  input:nth-of-type(2):checked ~ #carousel {
    --position: 2;
  }

  
</style>
