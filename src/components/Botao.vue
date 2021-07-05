<template>
  <button v-bind="$attrs"><slot/></button>
</template>

<!-- Quando queremos que o nosso comp receba atributos nativos do html e do Vue usamos a variavel $attrs -->
<!-- Essa variavel especial é um array contendo os valores passados para os atributos -->
<!-- O atributo v-bind do Vue consegue distribuir os valores para os atributos corretos -->

<!-- A tag <slot/> serve para que a valor passado entre as tags do comp seja enviado para onde essa tag está -->

<!-- Assim se um comp é construido da seguinte forma: <Botao type="text">Enviar<Botao/> -->
<!-- O btão dentro do tamplete recebe esses valores e seria equivalente ao seguinte código: -->
<!-- <button type="text">Enviar<button/> -->

<!-- Para exemplos de uso do comp Botao veja Formulario e Info -->
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