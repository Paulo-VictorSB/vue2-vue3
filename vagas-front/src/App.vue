<template>
  <div>
    <Header/>
    <MainContent/>
  </div>
</template>

<script>
import AppHeader from './components/layouts/AppHeader.vue'
import MainContent from './components/layouts/MainContent.vue'

export default {
  name: 'App',
  components: {
    Header: AppHeader,
    MainContent
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
  margin-top: 60px;
}
</style>
