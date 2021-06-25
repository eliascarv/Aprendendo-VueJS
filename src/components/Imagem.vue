<template>
  <img :src="src" :alt="descricao">
</template>

// Obs: os arquivos em na pasta public não precisam do caminho completo
// Basta comlocar o caminho a partir de public
<script>
export default {
  name: 'Imagem',
  data() {
    return {
      src: '/img/avatar.png',
      descricao: 'Avatar'
    }
  }
}
</script>