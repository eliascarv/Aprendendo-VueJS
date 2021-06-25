<template>
  <primeiro-comp />
  <life-cycle />
</template>

<script>
import PrimeiroComp from './components/PrimeiroComp.vue'
import LifeCycle from './components/LifeCycle.vue'

export default {
  name: 'App',
  components: {
    PrimeiroComp,
    LifeCycle
  }
}
</script>