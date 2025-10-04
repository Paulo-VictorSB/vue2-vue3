<template>
  <div class="container py-4">
    <div class="row">
      <div class="col">
        <h4>
          Apresente a sua vaga para milhares de profissionais gratuitamente
        </h4>
      </div>
    </div>

    <div class="row mt-3">
      <div class="col">
        <label class="form-label">Título da vaga</label>
        <input type="text" class="form-control" v-model="titulo" />
        <small class="text-muted"
          >Por exemplo: programador JavaScript e VueJS.</small
        >
      </div>
    </div>

    <div class="row mt-3">
      <div class="col">
        <label class="form-label">Descrição</label>
        <textarea class="form-control" v-model="descricao"></textarea>
        <small class="text-muted">Informe detalhes da vaga</small>
      </div>
    </div>

    <div class="row mt-3">
      <div class="col">
        <label class="form-label">Salário</label>
        <input type="number" class="form-control" v-model="salario" />
        <small class="text-muted">Informe o salário.</small>
      </div>

      <div class="col">
        <label class="form-label">Modalidade</label>
        <br />
        <select name="" id="modalidade" v-model="modalidade">
          <option value="" disabled>--Selecione</option>
          <option value="1">Home Office</option>
          <option value="2">Presencial</option>
        </select>
        <br />
        <small class="text-muted"
          >Informe onde as atividades serão realizadas.</small
        >
      </div>

      <div class="col">
        <label class="form-label">Tipo de contratação</label>
        <br />
        <select name="" id="tipo" v-model="tipo">
          <option value="" disabled>--Selecione</option>
          <option value="1">CLT</option>
          <option value="2">PJ</option>
        </select>
        <br />
        <small class="text-muted">Informe o tipo de contratação.</small>
      </div>
    </div>

    <div class="row mt-3">
      <div class="col">
        {{ titulo }} | {{ descricao }} | {{ salario }} | {{ modalidade }} |
        {{ tipo }} |
        <button type="submit" class="btn btn-primary" @click="cadastrarVaga">
          Cadastrar Vaga
        </button>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "PublicarVaga",
  data: () => ({
    titulo: "",
    descricao: "",
    salario: "",
    modalidade: "",
    tipo: "",
  }),
  methods: {
    cadastrarVaga() {
      let vagas = JSON.parse(localStorage.getItem("vagas"));

      if (!vagas) vagas = [];

      vagas.push({
        titulo: this.titulo,
        descricao: this.descricao,
        salario: this.salario,
        modalidade: this.modalidade,
        tipo: this.tipo,
      });

      localStorage.setItem("vagas", JSON.stringify(vagas));
    },
  },
};
</script>

<style>
</style>