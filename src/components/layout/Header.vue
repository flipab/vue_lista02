<template>
    <header class="header">
        <h1>Mercadex</h1>
        <p> Minha lista de compras em Vue.js | <a href="https://flipdesign.art.br/" target="_blank">Por Felipe Butzke</a></p>
         <div id="nav">
             <router-link to="/">Home</router-link> |
         <router-link to="/about">About</router-link>
         </div>
    </header>
</template>

<script >

export default {
    name: "Header"
    
}
</script>

<style scoped>

.header {
    background-color: royalblue;
    color: #fff;
    text-align: center;
    padding: 10px;
}

.header a {
    color: #fff;
    text-decoration: none;
    padding-right: 5px;
}

.nav {

    background-color: darkblue;
    color: dodgerblue;
}

</style>