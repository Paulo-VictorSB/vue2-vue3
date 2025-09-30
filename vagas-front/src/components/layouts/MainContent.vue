<template>
  <div class="container">
    <HomeView/>
    <publicarVaga/>
  </div>
</template>

<script>
import HomeView from '@/components/views/Home.vue'
import PublicarVaga from '@/components/views/PublicarVaga.vue'

export default {
  components: {
    HomeView,
    PublicarVaga
  }
}

</script>

<style>

</style>