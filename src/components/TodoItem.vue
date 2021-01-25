<template>
<div class="todo-item" v-bind:class="{'is-complete':todo.completed}">
     <p>
         <input type="checkbox" v-on:change="markComplete">
         {{todo.title}}
         <button @click="$emit('del-todo' , todo.id)" class="del">x</button> </p>
</div>
    
</template>

<script >
export default {
    name: "TodoItem",
    props: ["todo"],
    methods: {
        markComplete() {
            this.todo.completed = !this.todo.completed;
        }
    }
}
</script>

<style scoped>

.todo-item {
    background: #f4f4f4;
    padding: 2%;
    padding-left: 5%;
    padding-right: 5%;
    border-bottom: 1px #ccc dotted;
}
.is-complete {
    text-decoration: line-through;
}
.del {
background-color: #929292;
color: #fff;
border: none;
padding: 5px 9px;
border-radius: 50%;
cursor: pointer;
float: right;
    }


</style>