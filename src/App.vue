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
    <ul>
      <li>{{usuarios[0] }}</li>
      <li>{{usuarios[1] }}</li>
      <li>{{usuarios[2] }}</li>
      <li>{{usuarios[3] }}</li>
    </ul>
    <br>
    <ul>
      <li v-for="(usuario, index) in usuarios"> {{index}}: {{usuario}} </li>
    </ul>
    <br>
    <ul>
      <li v-for="(usuario, index) in usuarios" :key="index"> {{index}}:  {{usuario}} </li>
    </ul>
    <br>
    <ul>
      <li v-for="(valor, clave) in uusuarios" :key="clave">{{  clave }}: {{ valor }}</li>
    </ul>

    <hr />
    <h1>v-bind</h1>
    <img v-bin:src="url" alt="No hay internet">
  </div>

    <hr />
    <h1>v-on</h1>
    <div @dblclick="click" class="contador">Clicks: {{clicks}}</div>



</template>

<script>
  export default {
    data:() => ( {
      titulo:"Hola desde VUE.js 3",
      html: "<h3> Soy un H3 </h3>",
      edad: 0,
      usuarios: ["Melisa", "Fernando", "Raul", "Jose"],
      uusuarios: {nombre: "Yirsis"},
      clicks: 0,
      url:"https://cdn.svgporn.com/logos/descript-icon.svg",
    }),
    methods: {
      inc() {
        this.edad++;
      },
      dis () {
        this.edad--;
      },
      click() {
        this.clicks++;
      },
    },
  };
</script>

<style>
  div {
    text-align: center;
    margin: 0px 2rem;
  }
  h2 {
    color: tomato;
  }
  .contador {
    background: pink;
    color: snow;
    font-weight: bold;
    height: 400px;
  }
</style>