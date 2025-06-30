<template>
  <div class="carousel-container" id="projects">
    <h1>Projetos</h1>

    <ul class="carousel" ref="carousel">
      <li v-for="(project, index) in projects" :key="index">
        <ProjectCard :project="project" />
      </li>

    </ul>

    <div class="nav-buttons">
      <CircleBtn @click="prev">⮜</CircleBtn>
      <CircleBtn @click="next">⮞</CircleBtn>
    </div>
  </div>
</template>


<script setup>
import CircleBtn from '@/components/CircleBtn.vue'
import { ref } from 'vue';
  import projects from '@/assets/projects.json'
  import ProjectCard from './ProjectCard.vue'

  const carousel = ref(null);

  function next() {
    carousel.value?.scrollBy({ left: 320, behavior: 'smooth' });
  }

  function prev() {
    carousel.value?.scrollBy({ left: -320, behavior: 'smooth' });
  }
</script>

<style scoped>
  * {
    color: white;
  }

  ul {
    list-style: none;
    scrollbar-width: none;
    padding: 0;
  }

  body {
    background: #111;
    color: white;
  }

  h1 {
    text-align: center;
    margin-bottom: 1rem;
  }
  .carousel-container {
    margin: 28px;
  }
  .carousel {
    display: flex;
    gap: 1rem;
    overflow-x: auto;
    scroll-snap-type: x mandatory;
    scroll-behavior: smooth;
    padding-bottom: 1rem;
    padding: 0 28px;
  }

  .nav-buttons {
    margin-top: 2rem;
    display: flex;
    justify-content: center;
    gap: 1rem;
  }

</style>

