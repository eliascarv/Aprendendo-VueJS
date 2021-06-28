<template>
  <div>
    <p v-if="esta_trab">Estou trabalhando como {{ profissao }}.</p>
    <p v-else>Estou a procura de uma oportunidade.</p>
    <p>Meu email é: <span v-show="mostrar_email">{{ email }}</span></p>
    <button @click="showEmail">{{ texto_botao }}</button>
    <p>O link do meu perfil no github é o seguinte: <a v-bind:href="github">eliascarv</a></p>
    <Imagem />
    <Formulario />
  </div>
</template>

// Atributos Dinamicos: eles podem conter código vue. 
// É possivel tornar qualquer atributo de uma tag html passivel de receber código vue ou js
// Isso é possivel adicionando v-bind: antes do nome do atributo
// Como forma abreviada também é possivel simplismente adicionar : antes do nome do atributo
<script>
import Imagem from './Imagem.vue'
import Formulario from './Formulario.vue'

export default {
  name: 'Info',
  components: {
    Imagem,
    Formulario
  },
  data() {
    return {
      profissao: 'Programador',
      email: 'eliascarv@email.com',
      esta_trab: true,
      mostrar_email: false,
      texto_botao: 'Mostar Email',
      github: 'https://github.com/eliascarv'
    }
  },
  methods: {
    showEmail() {
      this.mostrar_email = !this.mostrar_email
      if(!this.mostrar_email) {
        this.texto_botao = 'Mostrar Email'
      } else {
        this.texto_botao = 'Esconder Email'
      }
    }
  }
}
</script>

<style scoped>
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