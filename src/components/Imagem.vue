<template>
  <img :src="src" :alt="descricao">
</template>

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