<template>
  <div class="project-card-container">
    <img :src="project.image" :alt="project.name" class="project-image"/>
    <div v-if="project.status === 'not-started' || project.status === 'in-progress'" class="status-overlay">
      <span>
        {{ project.status === 'not-started' ? 'Não iniciado' : 'Em progresso' }}
      </span>
    </div>
    
    <div class="project-content">
      <h2>{{ project.name }}</h2>
      <div class="tag-list">
        <TechnologiesTag
          v-for="tag in project.tags"
          :key="tag"
          :text="tag"
        />
      </div>
      
      <ul v-if="project.technologies && project.technologies.length" class="tec-list">
        <li v-for="tec in project.technologies" :key="tec">
          <img :src="getIconUrl(tec)" :alt="tec" class="tec-img" />


        </li>
      </ul>

      <div class="links-list">
        <RectBtn href="https://github.com/Andreivilla">GitHub</RectBtn>
        <RectBtn href="https://github.com/Andreivilla">Deploy</RectBtn>
      </div>

    </div>
  </div>
</template>

<script setup>
  import { defineProps, toRefs } from 'vue';
  import RectBtn from '@/components/RectBtn.vue'
  import TechnologiesTag from '@/components/TechnologiesTag.vue'

  const props = defineProps({
    project: {
      type: Object,
      required: true
    }
  });
  
  const { project } = toRefs(props);

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

  .links-list {
    width: 100%;
    display: flex;
    margin-top: 8px;
    gap: 8px;
    
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
    background: var(--gray-color);
    
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

  .status-overlay {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background-color: rgba(70, 70, 70, 0.5); /* cinza transparente */
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 1.2rem;
    font-weight: bold;
    color: white;
    z-index: 1;
    text-transform: uppercase;
    pointer-events: none; /* permite clicar nos elementos abaixo */
  }
  span {
    font-family: var(--primary-font-family);
    color: var(--primary-color);
    font-weight: 600; 
    font-size: 28px;
  }  
</style>