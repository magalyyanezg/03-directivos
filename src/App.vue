<template>
  <div>
    <h1>UNIVERSIDAD TECNOLÓGICA DE TEHUACÁN</h1>
    <hr />
    <h2> APW</h2>
    <h3>Grupo 4A</h3>
    <span v-text="'Hola desde la directiva v-text'"> </span>
    <br>
    <span>Hola desde la directiva v-text</span>
    <br>
    <span v-text="titulo"> </span>
    <br>
    Esta es una transmutación de texto ({{ titulo }}), con una variable prop <br>
    
  </div>
</template>

<script>
  export default {
    data:() => ( {
      titulo:"Hola desde VUE.js",

    }),
  };
</script>

<style>
  div {
    text-align: center;
    margin: 0px 2rem;
  }
</style>