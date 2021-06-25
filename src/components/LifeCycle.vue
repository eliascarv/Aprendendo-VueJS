<template>
  <h1>Meu nome é: {{ nome }}</h1>
</template>

// Quando o componete <life-cicle /> é criado, seu valor é alterado.
// Isso funciona graças ao método created()
// Assim, dados vindos do backend podem ser usados
// Existem vários outros eventos que podem ser usados para disparar modificações
// O método mouted() é um evendo que é disparado quando o componete é montado
<script>
export default {
  name: 'LifeCycle',
  data() {
    return {
      nome: ''
    }
  },
  created() {
    this.nome = 'Elias'
  }
}
</script>