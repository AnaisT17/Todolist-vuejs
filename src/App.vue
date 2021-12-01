<template>
  <img alt="todolist logo" src="./assets/work.jpg">
  <contenu></contenu>
  <header-top></header-top>
</template>

<script>
import Contenu from './components/Contenu.vue'

export default {
  name: 'App',
  components: {
    contenu: Contenu
  }
}
</script>


<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 30px;
  background-color: #EED7CE;
}
img{
  clip-path:circle(33% 50%);
  width: 30%;
  height: 30%;
  box-shadow: 12px 12px 2px 1px rgba(0, 0, 255, .2);
  border-radius: 10px;

}
</style>
