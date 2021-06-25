<template>
  <div>
    <h1>Hello Vue!</h1>
    <p>Meu nome é {{ nome }} e eu tenho {{ idade }} anos. </p>
  </div>
</template>

<script>
export default {
  name: "PrimeiroComp",
  data() {
    return {
      nome: "Elias",
      idade: 22
    }
  }
}
</script>