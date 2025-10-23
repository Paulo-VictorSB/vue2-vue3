<template>
  <div>
    <Header @navegarPara="switchView($event)" />
    <AlertaVue v-if="exibirAlerta"/>
    <MainContent :view="view" />
  </div>
</template>

<script>
import AppHeader from "@/components/layouts/AppHeader.vue";
import MainContent from "@/components/layouts/MainContent.vue";
import AlertaVue from "@/components/utils/Alerta.vue";

export default {
  name: "App",
  components: {
    Header: AppHeader,
    MainContent,
    AlertaVue,
  },
  data: () => ({
    view: "HomeView",
    exibirAlerta: false
  }),
  methods: {
    switchView(view) {
      this.view = view;
    },
  },
  mounted() {
    this.emitter.on("alerta", () => {
      this.exibirAlerta = true;
      setTimeout(() => this.exibirAlerta = false, 4000);
    });
  },
};
</script>
