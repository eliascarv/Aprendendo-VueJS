<template>
  <button v-bind="$attrs"><slot/></button>
</template>

<script>
export default {
  name: 'Botao'
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