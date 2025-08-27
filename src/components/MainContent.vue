<template>
  <main class="p-4 min-h-screen text-white
    bg-gradient-to-br from-[#1A0033] via-[#330066] to-[#4D0099]">
    <div class="flex flex-col items-center font-bold">
      <!--<h1 class="title font-montserrat"><span>Andrei Villa</span></h1>-->
      <h2 class="text-2xl text-primary">Desenvolvedor Full-Stack</h2>
      <p class="text-center">Formado em Ciência da Computação pela UDESC, estou em transição para me consolidar como desenvolvedor web full stack. 
      Com experiência em projetos que envolvem Vue.js, Node.js, bancos de dados e integrações com APIs, busco criar soluções 
      eficientes e centradas no usuário.</p>
    </div>
    <div class="mt-2 flex flex-col items-center">
      <div class="flex gap-4">
        <a href="https://www.linkedin.com/in/andrei-villa-7729801b6/" target="_blank"
          class="middle none center rounded-lg 
          bg-primary py-3 px-6 font-sans text-xs font-bold 
          uppercase text-white shadow-md shadow-blue-500/20 
          transition-all hover:shadow-lg hover:shadow-blue-500/40 
          focus:opacity-[0.85] focus:shadow-none active:opacity-[0.85] 
          active:shadow-none disabled:pointer-events-none disabled:opacity-50 
          disabled:shadow-none flex">
          <svg xmlns="http://www.w3.org/2000/svg" 
            fill="currentColor" 
            width="16" height="16" 
            class="mr-2" 
            viewBox="0 0 16 16">
            <path d="M0 1.146C0 .513.526 0 1.175 0h13.65C15.474 0 16 .513 16 1.146v13.708c0 .633-.526 1.146-1.175 1.146H1.175C.526 16 0 15.487 0 14.854zm4.943 12.248V6.169H2.542v7.225zm-1.2-8.212c.837 0 1.358-.554 1.358-1.248-.015-.709-.52-1.248-1.342-1.248S2.4 3.226 2.4 3.934c0 .694.521 1.248 1.327 1.248zm4.908 8.212V9.359c0-.216.016-.432.08-.586.173-.431.568-.878 1.232-.878.869 0 1.216.662 1.216 1.634v3.865h2.401V9.25c0-2.22-1.184-3.252-2.764-3.252-1.274 0-1.845.7-2.165 1.193v.025h-.016l.016-.025V6.169h-2.4c.03.678 0 7.225 0 7.225z"/>
          </svg>
          Linkedin
        </a>
        
        <a href="https://www.linkedin.com/in/andrei-villa-7729801b6/" target="_blank"
          class="middle none center rounded-lg 
            bg-primary py-3 px-6 font-sans text-xs font-bold 
            uppercase text-white shadow-md shadow-blue-500/20 
            transition-all hover:shadow-lg hover:shadow-blue-500/40 
            focus:opacity-[0.85] focus:shadow-none active:opacity-[0.85] 
            active:shadow-none disabled:pointer-events-none disabled:opacity-50 
            disabled:shadow-none flex">
          <svg xmlns="http://www.w3.org/2000/svg" 
            fill="currentColor" 
            width="16" height="16" 
            class="mr-2" 
            viewBox="0 0 16 16">
            <path d="M13.601 2.326A7.85 7.85 0 0 0 7.994 0C3.627 0 .068 3.558.064 7.926c0 1.399.366 2.76 1.057 3.965L0 16l4.204-1.102a7.9 7.9 0 0 0 3.79.965h.004c4.368 0 7.926-3.558 7.93-7.93A7.9 7.9 0 0 0 13.6 2.326zM7.994 14.521a6.6 6.6 0 0 1-3.356-.92l-.24-.144-2.494.654.666-2.433-.156-.251a6.56 6.56 0 0 1-1.007-3.505c0-3.626 2.957-6.584 6.591-6.584a6.56 6.56 0 0 1 4.66 1.931 6.56 6.56 0 0 1 1.928 4.66c-.004 3.639-2.961 6.592-6.592 6.592m3.615-4.934c-.197-.099-1.17-.578-1.353-.646-.182-.065-.315-.099-.445.099-.133.197-.513.646-.627.775-.114.133-.232.148-.43.05-.197-.1-.836-.308-1.592-.985-.59-.525-.985-1.175-1.103-1.372-.114-.198-.011-.304.088-.403.087-.088.197-.232.296-.346.1-.114.133-.198.198-.33.065-.134.034-.248-.015-.347-.05-.099-.445-1.076-.612-1.47-.16-.389-.323-.335-.445-.34-.114-.007-.247-.007-.38-.007a.73.73 0 0 0-.529.247c-.182.198-.691.677-.691 1.654s.71 1.916.81 2.049c.098.133 1.394 2.132 3.383 2.992.47.205.84.326 1.129.418.475.152.904.129 1.246.08.38-.058 1.171-.48 1.338-.943.164-.464.164-.86.114-.943-.049-.084-.182-.133-.38-.232"/>
          </svg>
            WhatsApp    
        </a>
      </div>
      <a 
        href="https://docs.google.com/document/d/1Pp05teT0m8-p8WDjk2MrAawFzUsT0-viwOCf4DHk9Hk/edit?usp=sharing" 
        class="middle none center mr-4 rounded-lg bg-primary py-3 px-6 
          font-sans text-xs font-bold uppercase text-white shadow-md 
          shadow-blue-500/20 transition-all hover:shadow-lg 
          hover:shadow-blue-500/40 focus:opacity-[0.85] focus:shadow-none 
          active:opacity-[0.85] active:shadow-none disabled:pointer-events-none 
          disabled:opacity-50 disabled:shadow-none m-2"
        :blank="true">
          Currículo
      </a>
    </div>
    <div class="m-2">
      <img src="../assets/images/perfil/perfil-pixel.gif" alt="">
    </div>
  </main>

</template>

<script setup>
  //import PerfilCarousel from './PerfilCarousel.vue';
  import RectBtn from './RectBtn.vue'
  import CircleBtn from './CircleBtn.vue';

  
</script>
<!--
<style scoped>

  .social-wrapper {
    display: flex;
    gap: 20px;
    align-items: center;
  }

  .social-circle {
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
    background: var(--bottom-gradient);
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
    /*background: var(--bottom-gradient);*/

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
      flex-direction: column;
    }
  }  

</style>
-->