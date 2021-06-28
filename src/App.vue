<template>
  <Header />
  <PrimeiroComp />
  <MultiplosEventos />
  <LifeCycle />
  <Info />
</template>

<script>
import PrimeiroComp from './components/PrimeiroComp.vue'
import LifeCycle from './components/LifeCycle.vue'
import Info from './components/Info.vue'
import Header from './components/Header.vue'
import MultiplosEventos from './components/MultiplosEventos.vue'

export default {
  name: 'App',
  components: {
    PrimeiroComp,
    LifeCycle,
    Info,
    Header,
    MultiplosEventos
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