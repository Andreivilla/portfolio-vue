<template>
  <main>
    <aside style="background-color: red;">
      <h2><span>Andrei Villa</span></h2>
      <h2>Desenvolvedor Full-Stack</h2>
      <p>Lorem ipsum, dolor sit amet consectetur adipisicing elit. Odit ad nemo in quis, maxime quae est fugiat unde cupiditate minus accusantium architecto repellat libero suscipit ducimus reprehenderit consequuntur blanditiis commodi.</p>

      <div class="social-wrapper">
        <a href="#"><img class="social-link" src="images/icons/social/linkedin.png" alt="linkedin-logo"></a>
        <a href="#"><img class="social-link" src="images/icons/social/instagram.png" alt="instagram-logo"></a>
        <a href="#"><img class="social-link" src="images/icons/social/whatsapp.png" alt="whatsapp-logo"></a>
      </div>

    </aside>
    
    <PerfilCarousel style="background-color: blue;"></PerfilCarousel>

  </main>
</template>

<script setup>
  import PerfilCarousel from './PerfilCarousel.vue';

</script>

<style scoped>
  * {
    font-family: 'Roboto';
    height: 100%;
  }
  main {
    display: flex;
    width: 100%;
  }
  aside {
    width: 50%; 
  } 
  PerfilCarousel {
    width: 20%;
  }

  /*adicionar aqui o media que some o perfil*/
  

</style>
