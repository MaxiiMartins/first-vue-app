<template>
  <div>
    <h1>Bienvenidos a </h1>
  </div>
  <div>
  <p :style="{color:colorText}" > {{ msg }} </p>
    <img src="./assets/vue.svg" class="logo" alt="Vue logo" />
  </div>
  <div>
    <h2> Los saluda {{ autor }}</h2>
  </div>
</template>

<!-- <script setup> para que dentro de el script me ahorro poner la importacion -->
<script setup>
  const msg = `Mi primer "Hola Mundo" en `.toUpperCase()
  const autor = "Maxi Martins"
  const colorText = "green"
</script>
<!-- <style scoped>  para que los estilos solo afecte a este componente -->
<style scoped>

div{
  font-family: 'Courier New', Courier, monospace;
  margin: 0;
  padding: 0;
  display: flex;
  justify-content: center;
  align-items: center;
  font-weight: bolder;
}
p{
  font-size: 2rem;
}
.logo {
  margin:1rem ;
  width: 3rem;
  height: auto;
}

</style>
