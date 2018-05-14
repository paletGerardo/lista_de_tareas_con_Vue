<template>

  <div>
    <h2>{{titulo}}</h2>
    <p>Tareas a realizar: {{numTareas}}</p>
  </div>

</template>

<script>

  export default {
    props: ['titulo', 'numTareas']
  }

</script>
