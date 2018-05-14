<template>
    <ul class="list-group">
      <hr>
      <li class="list-group-item col-12" v-for="(tarea, indice) of tareas" v-bind:class="{terminada: tarea.terminada }">
        <div class="row d-flex justify-content-between">
          <div>{{tarea.texto}}</div>
          <span>
          <button type="button" class="btn btn-success btn-xs" v-on:click="tarea.terminada = !tarea.terminada">V</button>
          <button type="button" class="btn btn-danger btn-xs" v-on:click="borrar(indice)">X</button>

        </span>
        </div>
      </li>
    </ul>
</template>

<script>
    export default {
        //name: "ListaTareaComponent"
      props: ['tareas'],

      methods: {
        borrar(indice){
          this.tareas.splice(indice,1);
        }
      }
    }
</script>

<style scoped>
  .terminada{
    color: gray;
    text-decoration: line-through;
  }
</style>
