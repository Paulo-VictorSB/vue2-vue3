<template>
  <div>
    <div
      class="offcanvas offcanvas-end"
      tabindex="-1"
      id="offcanvasRight"
      aria-labelledby="offcanvasRightLabel"
    >
      <div class="offcanvas-header">
        <h5 class="offcanvas-title" id="offcanvasRightLabel">
          Vagas Favoritas
        </h5>
        <button
          type="button"
          class="btn-close"
          data-bs-dismiss="offcanvas"
          aria-label="Close"
        ></button>
      </div>
      <div class="offcanvas-body">
        <ul class="list-group">
          <li class="list-group-item mb-3" v-for="(vaga, index) in vagas" :key="index">{{ vaga }}</li>
        </ul>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  mounted() {
    this.emitter.on("favoritarVaga", (e) => {
      this.vagas.push(e)
    });

    this.emitter.on("desfavoritarVaga", (e) => {
      let i = this.vagas.indexOf(e);
      if(i !== -1) this.vagas.splice(i, 1);
    });
  },
  data: () => ({
    vagas: []
  })
};
</script>

<style>
</style>