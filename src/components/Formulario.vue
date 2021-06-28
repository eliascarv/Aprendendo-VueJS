<template>
  <form @submit="enviarForm($event)">
    <input type="text" v-model="nome"><br>
    <input type="text" v-model="email"><br>
    <button type="submit">Enviar</button>
  </form>
</template>

<script>
export default {
  name: 'Formulario',
  data() {
    return {
      nome: '',
      email: ''
    }
  },
  methods: {
    enviarForm(evento) {
      evento.preventDefault()

      const nome = this.nome
      const email = this.email

      console.log('Form eviado')
      console.log('O nome é ' + nome)
      console.log('O email é ' + email)

      // Ajax
      // Salvar no DB
    }
  }
}
</script>

<style scoped>
input {
  height: 20px;
  margin-top: 5px;
  margin-bottom: 5px;
  border: solid rgba(0, 0, 0, 0.12) 2px;
  border-radius: 5px;
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

/* button:hover {
  background-color: rgba(0, 0, 0, 0.05);
} */

button:active {
  background-color: rgba(0, 0, 0, 0.05);
}
</style>