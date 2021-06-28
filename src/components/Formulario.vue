<template>
  <form @submit="enviarForm($event)">
    <input type="text" v-model="nome"><br>
    <input type="text" v-model="email"><br>
    <Botao type="submit">Enviar</Botao>
  </form>
</template>

<script>
import Botao from './Botao.vue'

export default {
  name: 'Formulario',
  components: {
    Botao
  },
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
</style>