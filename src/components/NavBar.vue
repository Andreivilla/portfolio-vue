<template>
  <header>
    <div class="title">
      <h1>Portifólio</h1>
      <h1>V 0.1</h1>
    </div>
      <nav>
        <input type="checkbox" id="sidebar-active">
        <label for="sidebar-active" class="open-sidebar-button">
          <svg xmlns="http://www.w3.org/2000/svg" height="32" viewBox="0 -960 960 960" width="32"><path d="M120-240v-80h720v80H120Zm0-200v-80h720v80H120Zm0-200v-80h720v80H120Z"/></svg>
        </label>
        <label id="overlay" for="sidebar-active"></label>
        <div class="links-container">
          <label for="sidebar-active" class="close-sidebar-button">
            <svg xmlns="http://www.w3.org/2000/svg" height="32" viewBox="0 -960 960 960" width="32"><path d="m256-200-56-56 224-224-224-224 56-56 224 224 224-224 56 56-224 224 224 224-56 56-224-224-224 224Z"/></svg>
          </label>

          <a class="home-link" href="index.html"><h3>Home</h3></a> 
          <a href="about.html"><h3>Abou</h3>t</a> 
          <a href="products.html"><h3>Products</h3></a>
          <a href="blog.html"><h3>Blog</h3></a>
          <a href="login.html"><h3>Login</h3></a>
          
        </div>
      </nav>
  </header>
</template>

<script setup>

</script>

<style scoped>
@import url("@/assets/fonts/fonts.css");

h1 {
  color: white;
  margin: 0;
}

.title {
  display: flex;
  gap: 0px;
  flex-direction: column;
}

header {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  align-items: center;
}

nav{
  height: 60px;
  display: flex;
  justify-content: flex-end;
  align-items: center;
}
.links-container{
  height: 100%;
  width: 100%;
  display: flex;
  flex-direction: row;
  align-items: center;
  gap: 8px;
}
nav a{
  height: 100%;
  display: flex;
  align-items: center;
  text-decoration: none;
  color: white;
}
nav a:hover{
  background-color: #A798FF;
}
nav .home-link{
  margin-right: auto;
}
nav svg{
  fill: white;
}
#sidebar-active{
  display: none;
}
.open-sidebar-button, .close-sidebar-button{
  display: none;
}

@media(max-width: 768px){
  .links-container{
    flex-direction: column;
    align-items: flex-start;

    position: fixed;
    top: 0;
    right: -100%;
    z-index: 10;
    width: 200px;

    background-color: #251D7A;
    transition: 0.75s ease-out;
  }
  nav a{
    box-sizing: border-box;
    height: auto;
    width: 100%;
    padding: 4px 20px;
    justify-content: flex-start;
  }
  .open-sidebar-button, .close-sidebar-button{
    padding: 20px;
    display: block;
  }
  #sidebar-active:checked ~ .links-container{
    right: 0;
  }
  #sidebar-active:checked ~ #overlay{
    height: 100%;
    width: 100%;
    position: fixed;
    top: 0;
    left: 0;
    z-index: 9;
  }
}
</style>
