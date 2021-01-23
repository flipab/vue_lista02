<template>
<div>
     <div v-bind:key="todo.id" v-for="todo in todos">
         <h3>{{todo.title}}</h3>
     </div>
</div>
    
</template>
<script lang="ts">
import Vue from 'vue'
export default Vue.extend({
    name: "Todos",
    props: ["todos"]
    
})
</script>
<style scoped>

</style>