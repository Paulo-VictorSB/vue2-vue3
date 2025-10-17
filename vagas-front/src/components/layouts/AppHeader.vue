<template>
  <header>
    <nav class="navbar navbar-expand-lg bg-dark navbar-dark fixed-top">
      <div class="container">
        <a class="navbar-brand" href="#">Vagas</a>
        <button
          class="navbar-toggler"
          type="button"
          data-bs-toggle="collapse"
          data-bs-target="#navbarSupportedContent"
          aria-controls="navbarSupportedContent"
          aria-expanded="false"
          aria-label="Toggle navigation"
        >
          <span class="navbar-toggler-icon"></span>
        </button>
        <div class="collapse navbar-collapse" id="navbarSupportedContent">
          <ul class="navbar-nav me-auto mb-2 mb-lg-0">
            <li class="nav-item">
              <a class="nav-link" @click="navegarPara('HomeView')" role="button"
                >Home</a
              >
            </li>
            <li class="nav-item">
              <a
                class="nav-link"
                @click="navegarPara('PublicarVaga')"
                role="button"
                >Publicar vaga</a
              >
            </li>
            <li class="nav-item">
              <a
                class="nav-link"
                role="button"
                data-bs-toggle="offcanvas"
                data-bs-target="#offcanvasRight"
                aria-controls="offcanvasRight"
                >Vagas Favoritas</a
              >
            </li>
          </ul>
        </div>
      </div>
    </nav>
    <VagasFavoritasVue />
  </header>
</template>

<script>
import VagasFavoritasVue from '@/components/utils/VagasFavoritas.vue';

export default {
  components: {
    VagasFavoritasVue
  },
  methods: {
    navegarPara(vaga) {
      this.$emit("navegarPara", vaga);
    },
  },
};
</script>
<style scoped>
a:hover {
  cursor: pointer;
}
</style>