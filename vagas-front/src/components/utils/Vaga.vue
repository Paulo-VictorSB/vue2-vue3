<template>
  <div class="card shadow">
    <div class="card-header bg-dark text-white">
      <div class="row">
        <div class="col d-flex justify-content-between">
          <div>
            {{ titulo }}
          </div>
          <div>
            <div class="form-check form-switch">
              <input
                type="checkbox"
                class="form-check-input"
                v-model="favoritada"
              />
              <label for="form-check-label">Favoritar</label>
            </div>
          </div>
        </div>
      </div>
    </div>
    <div class="card-body">{{ descricao }}</div>
    <div class="card-footer">
      <small class="text-muted">
        Sálario: R${{ salario }} | Modalidade: {{ getModalidade }} | Tipo:
        {{ getTipo }} | Publicação: {{ publicacao }}
      </small>
    </div>
  </div>
</template>

<script>
export default {
  name: "VagaVue",
  data: () => ({
    favoritada: false,
  }),
  watch: {
    favoritada(e) {
      e == true
        ? this.emitter.emit("favoritarVaga", this.titulo)
        : this.emitter.emit("desfavoritarVaga", this.titulo);
    },
  },
  props: {
    titulo: {
      type: String,
      required: true,
    },
    descricao: {
      type: String,
      default() {
        return "*".repeat(30);
      },
    },
    salario: {
      type: Number,
      required: true,
    },
    modalidade: {
      type: String,
      required: true,
    },
    tipo: {
      type: String,
      required: true,
    },
    publicacao: {
      type: String,
      required: true,
    },
  },
  computed: {
    getModalidade() {
      return this.modalidade == "1" ? "Home Office" : "Presencial";
    },
    getTipo() {
      return this.tipo == "1" ? "CLT" : "PJ";
    },
  },
};
</script>

<style>
</style>