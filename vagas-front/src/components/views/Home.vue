<template>
  <div>
    <p>Home</p>
  </div>
</template>

<script>
export default {
    name: "HomeView",
    activated() {
      console.log("Componente ativado")
    },
    deactivated() {
      console.log("Componente desativado")
    },
    beforeUnmount() {
      console.log("Antes de desmontar/destruir")
    },
    unmounted() {
      console.log("Desmontado/destruido")
    }

    // Caso você precise que a instancia do componente permaneca ativa você pode usar o lifecycle activated e deactivated, basicamente esse componente precisa ficar em cash. Melhor para performace.
}
</script>

<style>

</style>