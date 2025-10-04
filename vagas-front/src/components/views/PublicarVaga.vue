<template>
  <div class="container py-4">
    <div class="row">
      <div class="col">
        <h4>Apresente a sua vaga para milhares de profissionais gratuitamente</h4>
      </div>
    </div>

    <div class="row mt-3">
      <div class="col">
        <label class="form-label">Título da vaga</label>
        <input type="text" class="form-control">
        <small class="text-muted">Por exemplo: programador JavaScript e VueJS.</small>
      </div>
    </div>

    <div class="row mt-3">
      <div class="col">
        <label class="form-label">Descrição</label>
        <textarea class="form-control"></textarea>
        <small class="text-muted">Informe detalhes da vaga</small>
      </div>
    </div>

    <div class="row mt-3">
      <div class="col">
        <label class="form-label">Salário</label>
        <input type="number" class="form-control">
        <small class="text-muted">Informe o salário.</small>
      </div>

      <div class="col">
        <label class="form-label">Modalidade</label>
        <br>
        <select name="" id="modalidade">
          <option value="1">Home Office</option>
          <option value="2">Presencial</option>
        </select>
        <br>
        <small class="text-muted">Informe o salário.</small>
      </div>

      <div class="col">
        <label class="form-label">Tipo de contratação</label>
        <br>
        <select name="" id="tipo_de_contratacao">
          <option value="1">CLT</option>
          <option value="2">PJ</option>
        </select>
        <br>
        <small class="text-muted">Informe o tipo de contratação.</small>
      </div>
    </div>

    <div class="row mt-3">
      <div class="col">
        <button type="submit" class="btn btn-primary">Cadastrar Vaga</button>
      </div>
    </div>

  </div>
</template>

<script>
export default {
    name: "PublicarVaga"
}
</script>

<style>

</style>