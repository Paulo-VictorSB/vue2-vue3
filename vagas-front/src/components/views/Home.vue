<template>
  <div class="container py-4">
    <div class="row">
      <div class="col">
        <div class="h-100 bg-light p-5 border rounded-3">
          <h1>Pesquisar vagas</h1>

          <div class="row">
            <div class="col">
              <div class="form-group">
                <label>Título da vaga</label>
                <input type="text" class="form-control" placeholder="Pesquise por palvras chaves, Ex: 'PHP', 'Junior', 'Analista">
                <small class="form-text text-muted">Informe palavras que estejam relacionadas com o título que você procura.</small>
              </div>
            </div>
          </div>

          <div class="row">
            <div class="col">
              <button class="btn btn-outline-dark mt-2" type="button">Buscar</button>
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
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "HomeView",
};
</script>

<style>
</style>