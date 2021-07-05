<template>
  <h2>It is {{ date }}</h2>
</template>

<script>
export default {
  name: 'Relogio',

  data() {
    return {
      date: null
    }
  },

  methods: {
    tick() {
      this.date = new Date().toLocaleTimeString()
    }
  },

  mounted() {
    setInterval(this.tick, 1000)
  }
}
</script>










