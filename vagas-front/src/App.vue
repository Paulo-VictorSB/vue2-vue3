<template>
  <div>
    <h1>Componente App</h1>
    <button @click="desmontarComponente()">Desmontar o componente Conteudo</button>
    <Header/>
    <MainContent v-if="visibility"/>
  </div>
</template>

<script>
import AppHeader from '@/components/layouts/AppHeader.vue'
import MainContent from '@/components/layouts/MainContent.vue'

export default {
  name: 'App',
  components: {
    Header: AppHeader,
    MainContent
  },
  data: () => ({
    visibility: true 
  }),
  methods: {
    desmontarComponente() {
      this.visibility = false
    }
  }
}
</script>
