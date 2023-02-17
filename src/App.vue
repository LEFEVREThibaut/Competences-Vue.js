<template>
  <div id="app">
  <contenu></contenu>
  </div>
</template>

<script>
//import Header from "./components/Header.vue";
import TodoContenu from "./components/Contenu.vue";

export default {
  name: 'App',
  components: {
   // entete: Header,
    contenu : TodoContenu
  }
}

</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
