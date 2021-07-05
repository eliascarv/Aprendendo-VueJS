<template>
  <Header />
  <PrimeiroComp />
  <Relogio />
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
import Relogio from './components/Relogio.vue'

export default {
  name: 'App',
  components: {
    PrimeiroComp,
    LifeCycle,
    Pessoa,
    Header,
    MultiplosEventos,
    Formulario,
    Relogio
  }
}
</script>

// Qualquer CSS que não for scoped será global e valerá para todos os comps
// Assim, é boa prática colocar esse tipo de CSS apenas nos comps principais

<style>
@font-face {
  font-family: Inter;
  src: url('/fonts/Inter-VariableFont.ttf');
}

* {
  font-family: Inter, sans-serif;
}
</style>