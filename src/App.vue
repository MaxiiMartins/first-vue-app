<template>
  <div class="container" :style="{backgroundColor:bgColor,color:textColor}">
      <div>
        <h1>Bienvenidos a </h1>
    <p> {{ msg }} 
      <img src="./assets/vue.svg" class="logo" alt="Vue logo" />
    </p>
    <h2> Los saluda <span>{{ autor }} </span> </h2>
      <button style="margin: 1rem; padding:0.5rem; ;" @click="cambiarColor()" >Cambiar color</button>
      </div>
  </div>
</template>

<!-- <script setup> para que dentro de el script me ahorro poner la importacion -->
<script setup>
import {ref} from "vue" // sirve para crear una variable reactiva y se recargue cuando se modifica la variable
  const msg = `Mi primer "Hola Mundo" en `.toUpperCase()
  const autor = "Maxi Martins"
  let bgColor = ref("white")
  let textColor = ref("black")
  const cambiarColor = () =>{
    if(bgColor.value === "white"){
      bgColor.value = "black"
      textColor.value = "white"
    }else{
      bgColor.value = "white"
      textColor.value = "black"
    }
  }
</script>
<!-- <style scoped>  para que los estilos solo afecte a este componente -->
<style >
*{
  margin: 0;
  padding: 0;
}
.container{
  width: 100%;
  height: 100vh;
  font-family: 'Courier New', Courier, monospace;
  margin: 0;
  padding:0;
  display: flex;
  justify-content: center;
  align-items: center;
}

.logo {
  width: 2rem;
  height: auto;
}
</style>
