<template>
  <div>
    <h1>Pesquisar vagas</h1>
    <div class="row">
      <div class="col">
        <div class="form-group">
          <label>Título da vaga</label>
          <input
            type="text"
            class="form-control"
            placeholder="Pesquise por palvras chaves, Ex: 'PHP', 'Junior', 'Analista"
          />
          <small class="form-text text-muted"
            >Informe palavras que estejam relacionadas com o título que você
            procura.</small
          >
        </div>
      </div>
    </div>
    <div class="row">
      <div class="col">
        <button class="btn btn-outline-dark mt-2" type="button">Buscar</button>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "PesquisarVaga",
};
</script>

<style>
</style>