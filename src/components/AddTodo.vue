<template>
  <div>
      <form>
          <input type="text" placeholder="Adicione sua tarefa aqui">
          <input type="submit" value="Submit" class="btn">
      </form>
  </div>
</template>

<script >

export default {
    name: "AddTodo"
    
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