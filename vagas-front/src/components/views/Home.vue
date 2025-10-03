<template>
  <div class="container py-4">
    <div class="row">
      <div class="col">
        <div class="h-100 bg-light p-5 border rounded-3">
          <div class="row">
            <div class="col">
              <PesquisarVaga />
            </div>
          </div>
        </div>
      </div>
    </div>

    <div class="row mt-5">
      <div class="col-4">
        <IndicadorVue titulo="Vagas abertas" valor="100" />
      </div>

      <div class="col-4">
        <IndicadorVue titulo="Profissionais cadastrados" valor="225" />
      </div>

      <div class="col-4">
        <IndicadorVue
          titulo="Visitantes online"
          :valor="usuariosOnline"
          :alt="true"
        />
      </div>
    </div>

    <div class="row mt-5">
      <div class="col-6">
        <VagaVue />
      </div>
      <div class="col-6">
        <VagaVue />
      </div>
    </div>
  </div>
</template>

<script>
import PesquisarVaga from "@/components/utils/PesquisarVaga.vue";
import IndicadorVue from "@/components/utils/Indicador.vue";
import VagaVue from "@/components/utils/Vaga.vue";

export default {
  name: "HomeView",
  components: {
    PesquisarVaga,
    IndicadorVue,
    VagaVue,
  },
  data: () => ({
    usuariosOnline: 0,
  }),
  methods: {
    getUsuariosOnline() {
      this.usuariosOnline = Math.floor(Math.random() * 101);
    },
  },
  created() {
    this.getUsuariosOnline();
    setInterval(() => {
      this.getUsuariosOnline();
    }, 60000);
  },
};
</script>

<style>
</style>