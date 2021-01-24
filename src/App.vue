<template>
  <div id="app">
    <Header />
    <Todos v-bind:todos="todos" v-on:del-todo="deleteTodo" />
  </div>
</template>

<script>
import Header from './components/layout/Header';
import Todos from './components/Todos';

export default {
  name: 'App',
  components: {
    Header,
    Todos
    
  },//adicionando array de todos
  data() {
    return {
      todos: [ 
      {
        id: 1,
        title: "Ítem 01",
        completed: false
      },
       {
        id: 2,
        title: "Ítem 02",
        completed: false
      },
       {
        id: 3,
        title: "Ítem 03",
        completed: false
      }

      ]
    } 
  },
  methods: {
    deleteTodo(id) {
      this.todos = this.todos.filter(todo => todo.id !== id);
    }
  }
}
</script>

<style>
* {
  margin: 0;
  padding: 0;
}

body {
  font-family: Arial, Helvetica, sans-serif;
  line-height: 1.4;
}

</style>
