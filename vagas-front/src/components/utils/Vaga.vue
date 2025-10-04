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
    titulo: String,
    descricao: String,
    salario: Number,
    modalidade: String,
    tipo: String,
    publicacao: String,
  },
  created() {
    console.log(typeof this.titulo)
    console.log(typeof this.descricao)
    console.log(typeof this.salario)
    console.log(typeof this.modalidade)
    console.log(typeof this.tipo)
    console.log(typeof this.publicacao)
  }
};
</script>

<style>
</style>