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

// Eventos(v-on): os eventos são ações do usuario que podem jerar novos comportamentos
// Como acontece com o v-bind, @ é um alias para v-on

// Métodos: eles ficam na propriedade methods
// São funções que podem ser usadas para alterar as propriedades do comp
// Geralmente são usadas em eventos como @click (on:click)

// Props (propriedades): podem ser usadas da mesma forma que atributos html
// As props podem ser usadas no template da desma forma que os atributos de data(), usando {{}}
// Quando um novo comp é criado, pode-se passar valores para as props e os mesmos serão utilizados no comp
// O componet Info é usado no cmponente Pessoa, lá é possivel ver o uso das props
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