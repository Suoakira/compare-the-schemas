<template>
  <div id="app">
    <Root msg="Welcome to Your Vue.js App"/>
  </div>
</template>

<script>
import Root from './components/root.vue'
import './sass/_core.scss'

export default {
  name: 'App',
  components: {
    Root
  }
}
</script>

<style lang="scss">
 #app {
   background: white;
 }
</style>
