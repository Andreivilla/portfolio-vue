<template>
  <NavBar></NavBar>
  <MainContent></MainContent>
  <TechnologiesSection></TechnologiesSection>
  <ProjectCarousel></ProjectCarousel>
  
  
</template>

<script setup>
  import NavBar from "./components/NavBar.vue";
  import MainContent from "./components/MainContent.vue"; 
  import ProjectCarousel from "./components/ProjectCarousel.vue";
  import TechnologiesSection from "./components/TechnologiesSection.vue";


</script>

<style>
  @import url("@/assets/fonts/fonts.css");
  body {
    background-color: #0C122F;
    max-width: 1280px;
    margin: 0 auto;
    margin-top: 86px;

    /*
    margin-left: 25%;
    margin-right: 25%;*/
  }


</style>
