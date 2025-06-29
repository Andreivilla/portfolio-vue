<template>
  <main>
    <aside>
      <h1 class="title"><span>Andrei Villa</span></h1>
      <h1>Desenvolvedor Full-Stack</h1>
      <p>Lorem ipsum, dolor sit amet consectetur adipisicing elit. Odit ad nemo in quis, maxime quae est fugiat unde cupiditate minus accusantium architecto repellat libero suscipit ducimus reprehenderit consequuntur blanditiis commodi.</p>

      <div class="social-wrapper">
        <a class="btn" href="#contact">Contato</a>
        <a class="btn" href="">Currículo</a>
      </div>

    </aside>
    
    <div class="perfil-img-container">
      <img src="@/assets/images/perfil/perfil-pixel.gif" alt="">
    </div>
  </main>

</template>

<script setup>
  //import PerfilCarousel from './PerfilCarousel.vue';
  
</script>

<style scoped>
  
  .social-wrapper {
    display: flex;
    gap: 20px;
  }
  
  .btn {
    color: white;
    padding: 8px;
    border: 1px solid white;
    border-radius: 8px;
    background-color: #2940D3;

    font-family: 'Montserrat', sans-serif;
    font-weight: 500;
    font-size: 20px;
    
    transition: background-color 0.3s, color 0.3s;

  }

  .btn:hover {
    background-color: #1e32a5;
    color: white;
    border-color: #1e32a5;
    box-shadow: 0 0.5rem 1rem rgba(0, 0, 0, 0.15);
    transform: translateY(-2px); 
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
    padding-top: 60px;
  }

  .title {
    color: #A798FF;
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
