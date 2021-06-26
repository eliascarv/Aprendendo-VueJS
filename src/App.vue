<template>
  <Header />
  <PrimeiroComp />
  <LifeCycle />
  <Info />
</template>

<script>
import PrimeiroComp from './components/PrimeiroComp.vue'
import LifeCycle from './components/LifeCycle.vue'
import Info from './components/Info.vue'
import Header from './components/Header.vue'

export default {
  name: 'App',
  components: {
    PrimeiroComp,
    LifeCycle,
    Info,
    Header
  }
}
</script>

<style>
* {
  font-family: Inter, sans-serif;
}
</style>