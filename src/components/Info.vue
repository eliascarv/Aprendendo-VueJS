<template>
  <div>
    <p v-if="esta_trab">Estou trabalhando como {{ profissao }}.</p>
    <p v-else>Estou a procura de uma oportunidade.</p>
    <p v-show="mostrar_email">Meu email é: {{ email }}</p>
    <p>O link do meu perfil no github é o seguinte: <a v-bind:href="github">eliascarv</a></p>
    <imagem />
  </div>
</template>

// Atributos Dinamicos: eles podem conter código vue. 
// É possivel tornar qualquer atributo de uma tag html passivel de receber código vue ou js
// Isso é possivel adicionando v-bind: antes do nome do atributo
// Como forma abreviada também é possivel simplismente adicionar : antes do nome do atributo
<script>
import Imagem from './Imagem.vue'

export default {
  name: 'Info',
  components: {
    Imagem
  },
  data() {
    return {
      profissao: 'Programador',
      email: 'eliascarv@email.com',
      esta_trab: true,
      mostrar_email: true,
      github: 'https://github.com/eliascarv'
    }
  }
}
</script>