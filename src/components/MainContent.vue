<template>
  <main>
    <aside>
      <h1 class="title"><span>Andrei Villa</span></h1>
      <h1 class="sub-title">Desenvolvedor Full-Stack</h1>
      <p>Lorem ipsum, dolor sit amet consectetur adipisicing elit. Odit ad nemo in quis, maxime quae est fugiat unde cupiditate minus accusantium architecto repellat libero suscipit ducimus reprehenderit consequuntur blanditiis commodi.</p>

      <div class="social-wrapper">
        <RectBtn href="#contact">Contato</RectBtn>
        <RectBtn href="https://docs.google.com/document/d/1Pp05teT0m8-p8WDjk2MrAawFzUsT0-viwOCf4DHk9Hk/edit?usp=sharing" :blank="true">Currículo</RectBtn>
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
  
  .sub-title, p {
    color: var(--main-color);
  }

  a {
    text-decoration: none;
  }

  h1 {
    font-size: 2rem;
    margin: 0;
  }

  main {
    color: white;
    display: flex;
    align-items: center;
    width: 100%;
    height: 600px;
  }

  .title {
    background: var(--primary-gradient);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    background-clip: text; /* fallback pra navegadores compatíveis */
    color: transparent;
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
    align-items: center;
    justify-content: center;
    display: flex;
  }
  
  img {
    max-width: 80%;
    max-height: 80%;
    overflow: cover; 
    background: var(--bottom-gradient);

    display: flex;
    align-items: center;
    justify-content: center;
    border-radius: 0.5rem; /* opcional, pra dar um charme nos cantos */

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
