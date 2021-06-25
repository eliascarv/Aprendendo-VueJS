<template>
  <div>
    <p v-if="esta_trab">Estou trabalhando como {{ profissao }}.</p>
    <p v-else>Estou a procura de uma oportunidade.</p>
    <p v-show="mostrar_email">Meu email é: {{ email }}</p>
  </div>
</template>

<script>
export default {
  name: 'Info',
  data() {
    return {
      profissao: 'Programador',
      email: 'eliascarv@email.com',
      esta_trab: true,
      mostrar_email: true
    }
  }
}
</script>