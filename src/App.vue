<template>
  <div id="app">
  </div>
</template>

<script>

export default {
  name: 'App',
  components: {
    
  },//adicionando array de todos
  data() {
    return {
      todos: [ 
      {
        id: 1,
        title: "Todo 01",
        completed: true
      },
       {
        id: 2,
        title: "Todo 02",
        completed: true
      },
       {
        id: 3,
        title: "Todo 03",
        completed: true
      }

      ]
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
