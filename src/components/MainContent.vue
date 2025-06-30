<template>
  <main>
    <aside>
      <h1 class="title"><span>Andrei Villa</span></h1>
      <h1>Desenvolvedor Full-Stack</h1>
      <p>Lorem ipsum, dolor sit amet consectetur adipisicing elit. Odit ad nemo in quis, maxime quae est fugiat unde cupiditate minus accusantium architecto repellat libero suscipit ducimus reprehenderit consequuntur blanditiis commodi.</p>

      <div class="social-wrapper">
        <RectBtn href="#contact">Contato</RectBtn>
        <RectBtn href="/curriculo.pdf" :blank="true">Currículo</RectBtn>
      </div>

    </aside>
    
    <div class="perfil-img-container">
      <img src="@/assets/images/perfil/perfil-pixel.gif" alt="">
    </div>
  </main>

</template>

<script setup>
  //import PerfilCarousel from './PerfilCarousel.vue';
  import RectBtn from '@/components/RectBtn.vue'

  
</script>

<style scoped>
  
  .social-wrapper {
    display: flex;
    gap: 20px;
  }
  
  a {
    text-decoration: none;
  }

  h1 {
    font-size: 2rem;
  }

  main {
    color: white;
    display: flex;
    align-items: center;
    width: 100%;
    height: 600px;
  }

  .title {
    color: var(--secondary-color);
  }
  
  aside, .perfil-img-container  {
    width: 50%; 
    padding: 48px;
  } 
  PerfilCarousel {
    width: 20%;
  }

  .perfil-img-container {
    padding: 0 28px;
  }
  
  img {
    max-width: 100%;
    max-height: 100%;
    overflow: cover;
  }
  /*adicionar aqui o media que some o perfil*/
  @media(max-width: 768px){
    .perfil-img-container {
      display: none;
    }
    main {
      justify-content: center;
      align-items: center;
    }
    aside {
      text-align: center;
    }
    .social-wrapper {
      justify-content: center;
    }
  }  

</style>
