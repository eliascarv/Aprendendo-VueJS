<template>
  <Info :email="email" :profissao="profissao" :usr_github="usr_github" :link_github="link_github"/>
</template>

<script>
import Info from './Info.vue'

export default {
  name: 'Pessoa',
  components: {
    Info
  },
  data() {
    return {
      profissao: 'Programador',
      email: 'eliascarv@email.com',
      usr_github: 'eliascarv',
      link_github: 'https://github.com/eliascarv'
    }
  }
}
</script>