<template>
  <div>
    <p v-if="esta_trab">Estou trabalhando como {{ profissao }}.</p>
    <p v-else>Estou a procura de uma oportunidade.</p>
    <p>Meu email é: <span v-show="mostrar_email">{{ email }}</span></p>
    <Botao @click="showEmail">{{ texto_botao }}</Botao>
    <p>O link do meu perfil no github é o seguinte: <a v-bind:href="link_github">{{ usr_github }}</a></p>
    <Imagem />
  </div>
</template>

// Atributos Dinamicos: eles podem conter código vue. 
// É possivel tornar qualquer atributo de uma tag html passivel de receber código vue ou js
// Isso é possivel adicionando v-bind: antes do nome do atributo
// Como forma abreviada também é possivel simplismente adicionar : antes do nome do atributo
<script>
import Imagem from './Imagem.vue'
import Botao from './Botao.vue'

export default {
  name: 'Info',
  components: {
    Imagem,
    Botao
  },
  props: {
    profissao: String,
    email: String,
    usr_github: String,
    link_github: String
  },
  data() {
    return {
      esta_trab: true,
      mostrar_email: false,
      texto_botao: 'Mostar Email'
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