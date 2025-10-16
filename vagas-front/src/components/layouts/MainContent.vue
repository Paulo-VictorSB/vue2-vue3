<template>
  <div class="container">
    <transition name="fade" mode="out-in">
      <keep-alive>
        <component :is="view" />
      </keep-alive>
    </transition>
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
  data: () => ({}),
  props: {
    view: {
      required: true,
      type: String,
    },
  },
};
</script>

<style>
.fade-enter-active, .fade-leave-active {
  transition: opacity 0.3s;
}
.fade-enter-from, .fade-leave-to {
  opacity: 0;
}
</style>