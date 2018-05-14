<template>
    <ul class="list-group">
      <li class="list-group-item" v-for="(tarea, indice) of tareas">
        {{tarea.texto}}
        <span class="pull-right">
          <button type="button" class="btn btn-success btn-xs" v-on:click="tarea.terminada = !tarea.terminada">V</button>
          <button type="button" class="btn btn-danger btn-xs" v-on:click="borrar(indice)">V</button>

        </span>
      </li>
    </ul>
</template>

<script>
    export default {
        //name: "ListaTareaComponent"
      props: ['tareas'],
    }
</script>

<style scoped>

</style>
