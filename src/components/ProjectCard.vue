<template>
  <div class="project-card-container">
    <img :src="project.image" :alt="project.name" class="project-image"/>
    
    <div class="project-content">
      <h2>{{ project.name }}</h2>
      <ul class="tag-list">
        <li v-for="tag in project.tags" :key="tag" class="tag">{{ tag }}</li>
      </ul>
      
      <ul v-if="project.technologies && project.technologies.length" class="tec-list">
        <li v-for="tec in project.technologies" :key="tec">
          <img :src="getIconUrl(tec)" :alt="tec" class="tec-img" />
        </li>
      </ul>

      <ul class="links-list">
        <li>
          <a :href="project.github" target="_blank" rel="noopener noreferrer" class="tag">GitHub</a>
        </li>
        <li>
          <a :href="project.deploy" target="_blank" rel="noopener noreferrer" class="tag">Deploy</a>
        </li>
      </ul>

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


<style scoped>
  * {
    color: white;
  }

  .tag {
    border-radius: 3px;
    padding: .2em .5em .3em;
    border-radius: 12px;
    font-weight: 600;
    margin: .25em .1em;

    font-family: 'Montserrat', sans-serif;
    font-weight: 500; 
    font-size: 14px;   
  }

  .tag-list .tag {
    
    background-color: #A798FF;
  }

  .links-list a {
    text-decoration: none;
    
    background-color: #251D7A;
  }

  li {
    list-style: none;
  }

  ul {
    padding: 0;
    display: flex;
    flex-wrap: wrap;
    gap: 4px;
    scrollbar-width: none;

    margin-top: 12px;
  }

  .tec-img {
    width: 24px;
    height: 24px;
  }

  .project-card-container {
    height: 400px;
    width: 400px;

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
    background: #0B0E1E;
    
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
    
  }
  
</style>