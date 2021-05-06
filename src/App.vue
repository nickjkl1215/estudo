<template>
  <!-- <Primeiro curso="Fluencia em 10 dias" :detalhes="true" /> -->
  <div v-for="(cidade,i) in cidades" :key="i">
      <Primeiro :curso="cidade.name" :detalhes="cidade.exibirDetalhes"/>
  </div>
</template>

<script>
import Primeiro from "./components/Primeiro";

export default {
  name: "App",
  components: {
    Primeiro,
  },
  data() {
    return {
      cidades: [
        { name: "Salvador", exibirDetalhes: false },
        { name: "Roma", exibirDetalhes: true },
        { name: "Kiev", exibirDetalhes: false },
      ],
    };
  },
};
</script>

<style>
#app {
  margin: 0;
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
}
* {
  margin: 0;
}
</style>
