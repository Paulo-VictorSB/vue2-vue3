<template>
  <div class="container">
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