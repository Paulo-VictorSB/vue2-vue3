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
