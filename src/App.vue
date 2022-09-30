<template>
  <div>
    <h1>UNIVERSIDAD TECNOLÓGICA DE TEHUACÁN</h1>
    <hr />
    <h2> APW</h2>
    <h3>Grupo 4A</h3>
    <h1>Directivas en VUE.js</h1>
    <h1>v-html</h1>
    <div v-html="html"></div>
    <hr />
    <h1>v-show</h1>
    <h3>Tu edad es:  {{ edad }}</h3>
    <h2 v-if="edad >= 18 && edad > 0 && edad < 100">Mayor de edad</h2>
    <h2 v-if="edad < 18 && edad > 0 && edad < 100">Menor de edad</h2>
    <h2 v-else>Edad invalida</h2>
    <button @click="inc()">incrementar</button>
    <button @click="dis()">disminuir</button>

    <hr />
    <h1>v-for</h1>
  </div>
</template>

<script>
  export default {
    data:() => ( {
      titulo:"Hola desde VUE.js 3",
      html: "<h3> Soy un H3 </h3>",
      edad: 0,

    }),
    methods: {
      inc() {
        this.edad++;
      },
    },
  };
</script>

<style>
  div {
    text-align: center;
    margin: 0px 2rem;
  }
</style>