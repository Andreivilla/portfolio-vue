<template>
  <NavBar></NavBar>
  <MainContent></MainContent>
  <ProjectCarousel></ProjectCarousel>
  
  
</template>

<script setup>
  import NavBar from "./components/NavBar.vue";
  import MainContent from "./components/MainContent.vue"; 
  import ProjectCarousel from "./components/ProjectCarousel.vue";


</script>

<style>
  @import url("@/assets/fonts/fonts.css");
  body {
    background-color: #0C122F;
    /*
    margin-left: 25%;
    margin-right: 25%;*/
  }


</style>
