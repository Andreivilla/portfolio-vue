<template>
  <span :class="['tag', colorClass]">
    {{ text }}
  </span>
</template>

<script setup>
  import { computed } from 'vue'

  const props = defineProps({
    text: {
      type: String,
      required: true
    }
  })

  // Mapa de cores incluindo palavras compostas
  const colorMap = {
    'JavaScript': 'bg-yellow',
    'Pinia': 'bg-pinia',
    'Vue Router': 'bg-vue-router',
    'HTML': 'bg-orange',
    'Design Responsivo': 'bg-orange',
    'Temas': 'bg-blue',
    'Bootstrap': 'bg-blue',
    'API externa': 'bg-purple',
    'Machine Learning': 'bg-pink'
  }


  // Normaliza o texto antes de buscar a cor
  const normalizedText = computed(() => props.text.trim())

  const colorClass = computed(() => {
    return colorMap[normalizedText.value] || 'bg-gray'
  })
</script>

<style scoped>
  .tag {
    padding: 6px 12px;
    border-radius: 12px;
    color: white;
    font-weight: bold;
    font-size: 14px;
    display: inline-block;
  }
  .bg-pinia { background-color: #FFE064;}
  .bg-yellow { background-color: #f7df1e; color: #000; }
  .bg-green { background-color: #42b883; }
  .bg-orange { background-color: #f16529; }
  .bg-blue { background-color: #2965f1; }
  .bg-purple { background-color: #8e44ad; }
  .bg-pink { background-color: #e91e63; }
  .bg-gray { background-color: #777; }
  .bg-vue-router { background-color: #35495E; }
</style>
