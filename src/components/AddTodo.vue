<template>
  <div>
      <form @submit.prevent="addTodo">
          <input type="text" v-model="title" placeholder="Adicione sua tarefa aqui">
          <input type="submit" value="Submit" class="btn">
      </form>
  </div>
</template>

<script >
//import uuid from 'uuid';//removi pois o json placeholder já vem com id
export default {
    name: "AddTodo",
    data() {
        return {
            title: ''
        }
    },
    methods: {
        addTodo(e) {
            e.preventDefault();
            const newTodo = {
              //  id: uuid.v4(), //uuid pesquisar...cria id unica? //removi pois o json placeholder já vem com id
                title: this.title,
                completed: false 
            }
            //send up to parent
            this.$emit('add-todo', newTodo);
            
            this.title = '';
        }
    }
    
}
</script>

<style scoped>

form {
   display: flex;
   margin-top: 5%;
   margin-bottom: 5%;
   border: none;
}

input[type="text"] {
    flex: 10;
    padding: 5px;
    border: none;
    background-color: #f4f4f4;
    padding: 2%;

}

.btn {
    display: inline-block;
    border: none;
    background-color: royalblue;
    color: #fff;
    padding: 7px 20px;
    cursor: pointer;
}

.btn:hover {
    background-color: darkblue;
    color: dodgerblue;
}

input[type="submit"] {
    flex: 2;
}

</style>