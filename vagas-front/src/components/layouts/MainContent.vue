<template>
  <div class="container">
    <div class="m-2">
      <button @click="view = 'HomeView'" class="btn btn-outline-dark me-2">Home</button>
      <button @click="view = 'PublicarVaga'" class="btn btn-outline-dark">Publicar Vaga</button>
    </div>
    <keep-alive>
      <component :is="view" />
    </keep-alive>
  </div>
</template>

<script>
import HomeView from "@/components/views/Home.vue";
import PublicarVaga from "@/components/views/PublicarVaga.vue";

export default {
  components: {
    HomeView,
    PublicarVaga,
  },
  methods: {},
  data: () => ({
    view: "HomeView",
  }),
};
</script>

<style>
</style>