<template>
  <div class="carousel-container">
    <h1>Projetos</h1>

    <ul class="carousel" ref="carousel">
      <li v-for="(project, index) in projects" :key="index">
        <ProjectCard :project="project" />
      </li>

    </ul>

    <div class="nav-buttons">
      <button @click="prev">⮜</button>
      <button @click="next">⮞</button>
    </div>
  </div>
</template>


<script setup>
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

  body {
    background: #111;
    color: white;
    font-family: sans-serif;
  }

  h1 {
    text-align: center;
    margin-bottom: 1rem;
  }

  .carousel {
    display: flex;
    gap: 1rem;
    overflow-x: auto;
    scroll-snap-type: x mandatory;
    scroll-behavior: smooth;
    padding-bottom: 1rem;
  }

  .nav-buttons {
    margin-top: 1rem;
    display: flex;
    justify-content: center;
    gap: 1rem;
  }

  .nav-buttons button {
    background: #333;
    color: white;
    border: none;
    padding: 0.75rem 1rem;
    border-radius: 50%;
    font-size: 1.2rem;
    cursor: pointer;
    transition: background 0.3s;
  }

  .nav-buttons button:hover {
    background: #555;
  }
</style>

