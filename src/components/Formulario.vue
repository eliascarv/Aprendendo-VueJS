<template>
  <form @submit="enviarForm($event)">
    <input type="text" v-model="nome"><br>
    <input type="text" v-model="email"><br>
    <Botao type="submit">Enviar</Botao>
  </form>
</template>

// A variavel especial $event do Vue retorna o objeto do evento que está sendo usado
// Assim dentro da função usada no evento submit é possivel resetar o comportamento padrao do evento
// Isso é feito com o método preventeDefault
// Neste caso isso é usado para que ao enviar o form a página não recarregue
// Possibilitando assim que o form seja enviado ao DB sem que a págia recarregue

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