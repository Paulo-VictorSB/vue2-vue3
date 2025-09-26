<template>
  <div class="container">
    <HomeView/>
    <publicarVaga/>
  </div>
</template>

<script>
import HomeView from '../views/Home.vue'
import PublicarVaga from '../views/PublicarVaga.vue'

export default {
  components: {
    HomeView,
    PublicarVaga
  }
}

</script>

<style>

</style>