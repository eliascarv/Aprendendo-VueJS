<template>
  <div>
    <button @click="primeiro('Primeiro Evento'), segundo('Segundo Evento'), terceiro()">
      Ativar Multiplos Eventos
    </button>
    <p>{{ multiplos_eventos }}</p>
  </div>
</template>

<script>
export default {
  name: 'MultiplosEventos',
  data() {
    return {
      multiplos_eventos: ''
    }
  },
  methods: {
    primeiro(str) {
      this.multiplos_eventos = str
    },

    segundo(str) {
      setTimeout(() => this.multiplos_eventos = str, 1000)
    },

    terceiro() {
      setTimeout(() => this.multiplos_eventos = '', 2000)
    }
  }
}
</script>

<style scoped>
div {
  margin: 20px;
}

button {
  border: solid rgba(0, 0, 0, 0.12) 2px;
  background-color: white;
  height: 36px;
  min-width: 64px;
  border-radius: 5px;
  padding-left: 16px;
  padding-right: 16px;
}

button:active {
  background-color: rgba(0, 0, 0, 0.05);
}
</style>