<template>
  <div class="card shadow">
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
    titulo: {
      type: String,
      required: true
    },
    descricao: {
      type: String,
      required: true
    },
    salario: {
      type: Number,
      required: true,
      validator(prop) {
        let val = false
        Number(prop) < 3000 ? val = true : val = false;
        return val;
      }
    },
    modalidade: {
      type: String,
      required: true
    },
    tipo: {
      type: String,
      required: true
    },
    publicacao: {
      type: String,
      required: true
    },
  },
};
</script>

<style>
</style>