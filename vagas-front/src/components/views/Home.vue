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
        <IndicadorVue/>
      </div>

      <div class="col-4">
        <IndicadorVue/>
      </div>

      <div class="col-4">
        <IndicadorVue/> 
      </div>
    </div>
  </div>
</template>

<script>
import PesquisarVaga from "@/components/utils/PesquisarVaga.vue";
import IndicadorVue from '@/components/utils/Indicador.vue';

export default {
  name: "HomeView",
  components: {
    PesquisarVaga,
    IndicadorVue
  },
};
</script>

<style>
</style>