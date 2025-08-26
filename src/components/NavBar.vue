<template>
  <header class="lg:px-16 px-4 bg-black flex flex-wrap items-center shadow-md z-50">
    <div class="flex-1 flex justify-between items-center">
        <router-link to="/" class="font-logo text-4xl font-bold text-white">Andrei Villa</router-link>
    </div>
      <HamburgerMenu 
        class="md:hidden block"
        @changeMenu="changeMenu"
      /> 

    <div :class="menuOpen ? 'block' : 'hidden'" class="md:flex md:items-center md:w-auto w-full">
        <nav>
            <ul class="md:flex items-center justify-between text-base text-gray-700 pt-4 md:pt-0">
                <li><router-link to="/MafiaI" class="font-logo md:p-4 py-3 px-0 block text-white hover:text-primary-red text-2xl">
                    Home
                  </router-link>
                </li>
                <li><router-link to="/MafiaII" class="font-logo md:p-4 py-3 px-0 block text-white hover:text-primary-red text-2xl">
                    Contato
                  </router-link>
                </li>
                <li><router-link to="/MafiaIII" class="font-logo md:p-4 py-3 px-0 block text-white hover:text-primary-red text-2xl">
                    Projetos
                  </router-link>
                </li>
            </ul>
        </nav>
    </div>
  </header>

<!--
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
-->
</template>

<script setup>
  import { ref } from 'vue';
  import HamburgerMenu from './HamburgerMenu.vue';

  const menuOpen = ref(false);

  function changeMenu(){
    menuOpen.value = !menuOpen.value;
  }

</script>

