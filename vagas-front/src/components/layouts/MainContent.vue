<template>
  <div class="container">
    <h1>{{ titulo }}</h1>
    <button @click="atualizarComponente()">Atualizar</button>

    <!-- Renderizar os componentes de forma dinamica  -->

    <button @click="conteudo = 'HomeView' ">Home</button>
    <button @click="conteudo = 'PublicarVaga'">Publicar Vaga</button>
    
    <component :is="conteudo" />

    <!-- <HomeView/>
    <publicarVaga/> -->
  </div>
</template>

<script>
import HomeView from '@/components/views/Home.vue'
import PublicarVaga from '@/components/views/PublicarVaga.vue'

export default {
  components: {
    HomeView,
    PublicarVaga
  },
  methods: {
    atualizarComponente() {
      this.titulo += "*"
    }
  },
  data: () => ({
    teste: 'O componente foi criado',
    titulo: 'Componente conteudo',
    conteudo: 'HomeView'
  }),
  beforeCreate() {
    console.log("Antes de criar")
  },
  // Muito usando antes da criação (obvio) de um componente, mas no ambito de validar se o usuario está autênticado e afins.
  created() {
    console.log(this.teste)
  },
  // Quando o componente foi criado, você utiliza esse lifecycle para manipular os dados. NOTA: isso só é feito após toda a injeção de dependencias e reatividades.
  
  // Antes de consolidar a instância do vue com um componenete ele procura um EL(do vue2) e compila o html nele. E se tiver um template ele implementa os dados nesse componente.

  // Porém, antes de compilar o template e jogar no DOM final, nós temos a opção de tomar uma ação. e ela é feita através do lifecycle beforeMount()
  beforeMount() {
    console.log('Antes de montar o componente')  
  },
  // Esse lifecycle é bastante utilizado para fazer uma requisição http para o backend e retornar os dados para recuperar dados para compor o nosso template.

  // Quando o vue monta de fato o template já compilado dentro de um elemento html ele aciona o lifecycle mounted() indicando assim que o componente foi montado.]
  mounted() {
    console.log('Componente Montado')
  },

  // beforeUpdate e updated são gatilhos disparados no componente antes e após uma atualização do mesmo.
  beforeUpdate() {
    console.log('Antes de atualizar')
  },
  updated() {
    console.log('Atualizado')
  },

  // beforeUnmout e unmounted são gatilhso disparados no componente antes e após a desmontagem do componente
  beforeUnmount() {
    console.log("Componente MainContent antes de ser destruido")
  },
  unmounted() {
    console.log("Componente MainContent destruido")
  }
}

</script>

<style>

</style>