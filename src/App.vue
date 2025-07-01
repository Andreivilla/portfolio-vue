<template>
  <NavBar></NavBar>
  <MainContent></MainContent>
  <TechnologiesSection></TechnologiesSection>
  <ProjectCarousel></ProjectCarousel>
  <FooterContent></FooterContent>
  
  
</template>

<script setup>
  import NavBar from "./components/NavBar.vue";
  import MainContent from "./components/MainContent.vue"; 
  import ProjectCarousel from "./components/ProjectCarousel.vue";
  import TechnologiesSection from "./components/TechnologiesSection.vue";
  import FooterContent from "./components/FooterContent.vue";


</script>

<style>
  @import url("@/assets/fonts/fonts.css");
  body {
    /*background-color: #0C122F;*/
    background-color: var(--bg-main-color);
    max-width: 1280px;
    margin: 0 auto;
    margin-top: 86px;

    
  }


</style>
