<template>
  <a
    :href="href"
    class="rect-btn"
    :target="blank ? '_blank' : '_self'"
  >
    <slot />
  </a>
</template>

<script setup>
  defineProps({
    href: {
      type: String,
      required: true,
    },
    blank: {
      type: Boolean,
      default: false,
    },
  })
</script>

<style scoped>
  .rect-btn {
    color: white;
    padding: 8px;
    border: 1px solid white;
    border-radius: 8px;
    background-color: #2940D3;

    font-family: 'Montserrat', sans-serif;
    font-weight: 500;
    font-size: 20px;
    
    transition: background-color 0.3s, color 0.3s;
    text-decoration: none;
  }

  .rect-btn:hover {
    background-color: #1e32a5;
    color: white;
    border-color: #1e32a5;
    box-shadow: 0 0.5rem 1rem rgba(0, 0, 0, 0.15);
    transform: translateY(-2px); 
  }
</style>