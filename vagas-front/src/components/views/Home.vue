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
        <div class="h-100 p-5 border rounded-3 bg-dark text-white">
          <p>Vagas abertas</p>
          <h2>25</h2>
        </div>
      </div>

      <div class="col-4">
        <div class="h-100 p-5 border rounded-3 bg-dark text-white">
          <p>Profissionais cadastrados</p>
          <h2>125</h2>
        </div>
      </div>

      <div class="col-4">
        <div class="h-100 p-5 border rounded-3 bg-light text-dark">
          <p>Visitantes online</p>
          <h2>15</h2>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import PesquisarVaga from "@/components/utils/PesquisarVaga.vue";

export default {
  name: "HomeView",
  components: {
    PesquisarVaga,
  },
};
</script>

<style>
</style>