<template>
  <div>
    <Header @navegarPara="switchView($event)"/>
    <MainContent
      :view=view
    />
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
    view: "HomeView"
  }),
  methods: {
    switchView(view) {
      this.view = view
    }
  },
}
</script>
