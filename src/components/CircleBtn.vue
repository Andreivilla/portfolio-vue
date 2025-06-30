<template>
  <a
    :href="href"
    :target="blank ? '_blank' : '_self'"
    class="circle-btn"
    aria-label="Social link"
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
.circle-btn {
  background-color: #2940D3;
  color: white;
  border: none;
  padding: 1.2rem;
  border-radius: 50%;
  font-size: 1.5rem;
  cursor: pointer;
  transition: background 0.3s;
  display: inline-flex;
  align-items: center;
  justify-content: center;
  width: 1.5rem;
  height: 1.5rem;
  text-decoration: none;
}

.circle-btn:hover {
  background-color: #1e32a5;
  box-shadow: 0 0.5rem 1rem rgba(0, 0, 0, 0.15);
  transform: translateY(-2px); 
}

.circle-btn svg {
  height: 90%;
  width: 90%;
}
</style>
