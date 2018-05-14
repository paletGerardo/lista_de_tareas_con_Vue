<template>
  <div id="app" class="container">
    <div class="jumbotron">
      <titulo v-bind:titulo = "titulo"></titulo>
      <nueva-tarea v-bind:tareas="tareas"></nueva-tarea>
    </div>
  </div>
</template>

<script>
  // importar componente TituloComponent
  import Titulo from './TituloComponent.vue'
  import NuevaTarea from './NuevaTareaComponent.vue'

  export default {
    // los componentes que voy a utilizar
    components: {
      Titulo,
      NuevaTarea,
    },

    //los datos que voy a usar
    data () {
      return {

        titulo: '- Lista de tareas -',

        tareas: [
          {
            texto: 'Aprender Vue.js',
            terminada: false,
          },

          {
            texto: 'Aprender Vue.js',
            terminada: false,
          },

          {
            texto: 'Aprender Vue.js',
            terminada: false,
          },
        ]
      }
    }
  }
</script>







































<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

h1, h2 {
  font-weight: normal;
}

ul {
  list-style-type: none;
  padding: 0;
}

li {
  display: inline-block;
  margin: 0 10px;
}

a {
  color: #42b983;
}
</style>
