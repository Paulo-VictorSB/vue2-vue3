<template>
  <div class="card shadow">
    <div class="card-header bg-dark text-white">{{ titulo }}</div>
    <div class="card-body">{{ descricao }}</div>
    <div class="card-footer">
      <small class="text-muted">
        Sálario: R${{ salario }} | Modalidade: {{ getModalidade }} |
        Tipo: {{ getTipo }} | Publicação: {{ publicacao }}
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
      default() {
        return "*".repeat(30);
      }
    },
    salario: {
      type: Number,
      required: true,
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
  computed: {
    getModalidade() {
      return this.modalidade == "1" ? 'Home Office' : 'Presencial';
    },
    getTipo() {
      return this.tipo == "1" ? 'CLT' : 'PJ';
    }
  }
};
</script>

<style>
</style>