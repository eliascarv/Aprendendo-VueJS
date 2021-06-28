<template>
  <Header />
  <PrimeiroComp />
  <MultiplosEventos />
  <LifeCycle />
  <Pessoa />
  <Formulario />
</template>

<script>
import PrimeiroComp from './components/PrimeiroComp.vue'
import LifeCycle from './components/LifeCycle.vue'
import Pessoa from './components/Pessoa.vue'
import Header from './components/Header.vue'
import MultiplosEventos from './components/MultiplosEventos.vue'
import Formulario from './components/Formulario.vue'

export default {
  name: 'App',
  components: {
    PrimeiroComp,
    LifeCycle,
    Pessoa,
    Header,
    MultiplosEventos,
    Formulario
  }
}
</script>

<style>
@font-face {
  font-family: Inter;
  src: url('/fonts/Inter-VariableFont.ttf');
}

* {
  font-family: Inter, sans-serif;
}
</style>