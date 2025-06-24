<template>
  <div class="project-card-container">
    <img :src="project.image" :alt="project.name" class="project-image"/>
    
    <div class="project-content">
      <h2>{{ project.name }}</h2>
      <ul class="tag-list">
        <li v-for="tag in project.tags" :key="tag">{{ tag }}</li>
      </ul>
      
      <ul v-if="project.technologies && project.technologies.length" class="tec-list">
        <li v-for="tec in project.technologies" :key="tec">
          <img :src="getIconUrl(tec)" :alt="tec" class="tec-img" />
        </li>
      </ul>

      <div class="links">
        <a :href="project.github" target="_blank" rel="noopener noreferrer">GitHub</a>
        <a :href="project.deploy" target="_blank" rel="noopener noreferrer">Deploy</a>
      </div>
    </div>
  </div>
</template>

<script setup>
  import { defineProps, toRefs } from 'vue';

  

  const props = defineProps({
    project: {
      type: Object,
      required: true
    }
  });
  

  const { project } = toRefs(props);

// Importa as imagens manualmente ou via require.context
const requireIcon = require.context('@/assets/images/icons/techs', false, /\.(png|svg)$/)

function getIconUrl(name) {
  try {
    return requireIcon(`./${name}.png`)
  } catch {
    return '' // fallback caso não encontre
  }
}

</script>


<style>

  ul {
    list-style: none;
    padding: 0;
    display: flex;
    gap: 4px;
    scrollbar-width: none;
  }

  .tec-img {
    width: 24px;
    height: 24px;
  }

  .project-card-container {
    height: 300px;
    width: 300px;

    flex: 0 0 300px;
    scroll-snap-align: center;
    background: #222;
    border-radius: 1rem;
    overflow: hidden;
    display: flex;
    flex-direction: column;
    position: relative;
  }

  .project-image{
    object-fit: cover;
  }

  .project-card-container:hover .project-content {
    transform: translateY(0%);
  }

  .project-content {
    position: absolute;
    bottom: 0;
    left: 0;
    width: 100%;
    background: rgba(0, 0, 0, 0.85);
    color: white;
    padding: 1rem;
    transform: translateY(70%);
    transition: transform 0.4s ease;
  }

  .project-content h2 {
    margin: 0 0 0.5rem;
    font-size: 1.2rem;
  }

  .project-content p {
    margin: 0;
    font-size: 0.9rem;
    color: #ccc;
  }
  
</style>