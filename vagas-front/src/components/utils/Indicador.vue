<template>
  <div :class="classAlt">
    <p>{{ titulo }}</p>
    <h2>{{ valor }}</h2>
  </div>
</template>

<script>
export default {
  name: "IndicadorVue",
  computed: {
    classAlt() {
      return this.alt ? "h-100 p-5 border rounded-3 bg-light text-dark" : "h-100 p-5 border rounded-3 bg-dark text-white";
    },
  },
  props: {
    titulo: String,
    valor: String,
    alt: Boolean
  },
};
</script>

<style>
</style>