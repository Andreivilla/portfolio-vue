<template lang="">
  <footer>
    <div class="footer-line"></div>
    <ContactLinks></ContactLinks>
    
  </footer>
</template>

<script setup>
  import ContactLinks from './ContactLinks.vue';

</script>

<style>
  footer {
    margin: 28px;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    padding-top: 1rem;
  }
  .footer-line {
    width: 100%;
    height: 1px;
    background-color: white;
    margin: 2rem 0;
  }

</style>