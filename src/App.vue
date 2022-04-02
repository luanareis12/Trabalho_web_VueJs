<template>
<h1 class="text-center">Conversor de Moedas</h1>
  <div id="app"><!-- contendo todos os conversores criados-->
    <div class="linha">
      <ConversorM moeda-a="USD" moeda-b="BRL"/>
      <ConversorM moeda-a="BRL" moeda-b="USD"/>
    </div>
    <div class="linha">
      <ConversorM moeda-a="EUR" moeda-b="BRL"/>
      <ConversorM moeda-a="BRL" moeda-b="EUR"/>
    </div>
    <div class="linha">
      <ConversorM moeda-a="CAD" moeda-b="BRL"/>
      <ConversorM moeda-a="BRL" moeda-b="CAD"/>
    </div>
  </div>
  
</template>

<script>
import ConversorM from "./components/ConversorM.vue"; //endereço do componente conversor
//declarando que será utlizado o componente conversor
export default {
  name: "app",
  components: {
    ConversorM
  }
};
</script>

<style>
#app {
  margin: auto;
  max-block-size: 900px;
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #000000;
  margin-top: 60px;
}
.linha{
  margin-top: 40px;
  display: flex;
  justify-content: space-around;
}

.text-center{
  text-align: center;
}
</style>
