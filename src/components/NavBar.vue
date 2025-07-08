<template>
  <header>
    <div class="nav-container">
      <div class="title">
        <h1>Andrei Villa</h1>
      </div>
        <nav>
          <input type="checkbox" id="sidebar-active">
          <label for="sidebar-active" class="open-sidebar-button">
            <svg xmlns="http://www.w3.org/2000/svg" height="32" viewBox="0 -960 960 960" width="32"><path d="M120-240v-80h720v80H120Zm0-200v-80h720v80H120Zm0-200v-80h720v80H120Z"/></svg>
          </label>
          <label id="overlay" for="sidebar-active"></label>
          <div class="links-container">
            <label for="sidebar-active" class="open-sidebar-button">
              <svg xmlns="http://www.w3.org/2000/svg" height="32" viewBox="0 -960 960 960" width="32"><path d="m256-200-56-56 224-224-224-224 56-56 224 224 224-224 56 56-224 224 224 224-56 56-224-224-224 224Z"/></svg>
            </label>
            
            <a href=""><router-link to="/"><h3>Home</h3></router-link></a>
            <a href="#contact"><h3>Contato</h3></a> 
            <a href="#projects"><h3>Projetos</h3></a>
            <ThemeToggle/>
          </div>
        </nav>
      </div>
  </header>
</template>

<script setup>
import ThemeToggle from './ThemeToggle.vue';

</script>

<style scoped>
  @import url("@/assets/fonts/fonts.css");

  header {
    position: fixed;
    width: 100%;
    top: 0;
    left: 0;
    
    z-index: 1000; /* pra ficar acima de tudo */    
    margin: 0;
    padding: 0;
  }

  .nav-container {
    max-width: 1280px;
    margin: 0 auto;
    padding: 12px 22px;
    display: flex;
    justify-content: space-between;
    align-items: center;
    background-color: var(--bg-main-color)
  }

  h1 {
    color: white;
    margin: 0;
  }

  .title h1 {
    display: flex;
    gap: 0px;
    flex-direction: column;
    color: var(--primary-color);
  }
  nav{
    height: 60px;
    display: flex;
    justify-content: flex-end;
    align-items: center;
  }
  .links-container{
    height: 100%;
    width: 100%;
    display: flex;
    flex-direction: row;
    align-items: center;
    gap: 8px;
  }
  nav a{
    height: 100%;
    display: flex;
    align-items: center;
    text-decoration: none;
    color: var(--main-color);
  }

  nav a:hover{
    color: var(--primary-color);
  }

  nav .home-link{
    margin-right: auto;
  }

  #sidebar-active{
    display: none;
  }
  .open-sidebar-button, .close-sidebar-button{
    display: none;
  }

  svg {
    fill: var(--main-color);
    height: 48px;
    width: 48px;
  }

  svg:hover {
    fill: var(--primary-color);
  }

  @media(max-width: 768px){
  

    .links-container{
      flex-direction: column;
      align-items: flex-start;

      position: fixed;
      top: 0;
      right: -100%;
      z-index: 10;
      width: 200px;

      background-color: var(--bg-main-color);
      transition: 0.75s ease-out;
    }
    nav a{
      box-sizing: border-box;
      height: auto;
      width: 100%;
      padding: 4px 20px;
      justify-content: flex-start;
    }
    nav img {
      filter: invert(100%);
      height: 32px;
      width: 32px;
    }
    .open-sidebar-button, .close-sidebar-button{
      padding: 20px;
      display: block;
    }
    #sidebar-active:checked ~ .links-container{
      right: 0;
    }
    #sidebar-active:checked ~ #overlay{
      height: 100%;
      width: 100%;
      position: fixed;
      top: 0;
      left: 0;
      z-index: 9;
    }
  }
</style>
