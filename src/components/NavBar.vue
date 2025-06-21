<template>
  <header>
    <div id="title">
      <h1>Portifólio</h1>
      <h1>V 0.1</h1>
    </div>
    <nav>
      <div class="mobile-menu">
        <div class="line1"></div>
        <div class="line2"></div>
        <div class="line3"></div>
      </div>
      <ul class="nav-list">
        <li class="nav-item"><a href="#">Início</a></li>
        <li class="nav-item"><a href="#">Serviços</a></li>
        <li class="nav-item"><a href="#">Sobre</a></li>
        <li class="nav-item"><a href="#">Contato</a></li>
        <li class="nav-item"><a href="#" id="inscreva-se-btn">Já tem uma conta?</a></li>
      </ul>
    </nav>
  </header>
</template>

<script setup>


</script>

<style scoped>
  header {
    font-family: 'Roboto';
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    align-items: center;
  }

  ul {
    display: flex;
    justify-content: space-between;
    list-style: none;
  }
  a {
    color: white;
   text-decoration: none; 
  }

  li {
    margin: 10px;
  }

  .mobile-menu {
    display: none;
  }
</style>
