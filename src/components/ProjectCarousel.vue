<template>
  <div class="carousel-container" id="projects">
    <h1>Projetos</h1>

    <ul class="carousel" ref="carousel">
      <li v-for="(project, index) in projects" :key="index">
        <ProjectCard :project="project" />
      </li>

    </ul>

    <div class="nav-buttons">
      <CircleBtn @click="prev">
        <svg xmlns="http://www.w3.org/2000/svg" fill="currentColor" class="bi bi-caret-left-fill" viewBox="0 0 16 16">
          <path d="m3.86 8.753 5.482 4.796c.646.566 1.658.106 1.658-.753V3.204a1 1 0 0 0-1.659-.753l-5.48 4.796a1 1 0 0 0 0 1.506z"/>
        </svg>
      </CircleBtn>
      
      <CircleBtn @click="next">
        <svg xmlns="http://www.w3.org/2000/svg" fill="currentColor" class="bi bi-caret-right-fill" viewBox="0 0 16 16">
          <path d="m12.14 8.753-5.482 4.796c-.646.566-1.658.106-1.658-.753V3.204a1 1 0 0 1 1.659-.753l5.48 4.796a1 1 0 0 1 0 1.506z"/>
        </svg>
      </CircleBtn>
    </div>
  </div>
</template>


<script setup>
import CircleBtn from '../components/CircleBtn.vue'
import { ref } from 'vue';
  import projects from '../assets/projects.json'
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

