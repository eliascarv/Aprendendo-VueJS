<template>
  <primeiro-comp />
  <life-cycle />
  <info />
</template>

<script>
import PrimeiroComp from './components/PrimeiroComp.vue'
import LifeCycle from './components/LifeCycle.vue'
import Info from './components/Info.vue'

export default {
  name: 'App',
  components: {
    PrimeiroComp,
    LifeCycle,
    Info
  }
}
</script>