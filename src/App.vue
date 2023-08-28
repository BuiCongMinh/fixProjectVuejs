<template>
  <div class="app">
    <Header/>
    xin chao  
    <Todos/>
  </div>
</template>

<script>
import Header from './components/Header.vue'
import Todos from './components/Todos.vue'

export default {
  name: "App",
  components: {Header,Todos}
}

</script>

<style>
  #app{
    font-family: Avener,Arial, Helvetica, sans-serif;
  }
</style>