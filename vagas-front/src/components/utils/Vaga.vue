<template>
  <div class="card">
    <div class="card-header bg-dark text-white">{{ titulo }}</div>
    <div class="card-body">{{ descricao }}</div>
    <div class="card-footer">
      <small class="text-muted">
        Sálario: R${{ salario }} | Modalidade: {{ modalidade }} |
        Tipo: {{ tipo }} | Publicação: {{ publicacao }}
      </small>
    </div>
  </div>
</template>

<script>
export default {
  name: "VagaVue",
  props: {
    titulo: String,
    descricao: String,
    salario: String,
    modalidade: String,
    tipo: String,
    publicacao: String,
  },
};
</script>

<style>
</style>