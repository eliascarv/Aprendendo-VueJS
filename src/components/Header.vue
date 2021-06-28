<template>
  <ul>
    <li><a href="#">Início</a></li>
    <li><a href="#">Contato</a></li>
    <li><a href="#">História</a></li>
  </ul>
</template>

<script>
export default {
  name: 'Header'
}
</script>

// Quando o CSS é definido como scoped, o mesmo só é aplicado ao comp ao qual pertece
<style scoped>
  ul {
    list-style: none;
    display: flex;
  }

  li {
    margin: 10px;
  }

  a {
    padding: 5px;
    color: red;
    text-decoration: none;
    border: solid red 2px;
    border-radius: 5px;
  }

  a:visited {
    color: red;
  }

  a:hover {
    color: white;
    background-color: red;
  }
</style>