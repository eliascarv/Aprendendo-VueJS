// Em tempalte, se ouver mais de uma tag elas devem ficar dentro de uma div
<template>
  <div>
    <h1>Hello Vue!</h1>
    <p>Meu nome é {{ nome }}, eu tenho {{ idade }} anos. </p>
  </div>
</template>

// Entre algumas das propriedades mais importantes de um componente está o name
// O name define o nome do componete, o padrão é usar o estilo camelo
// Porém quando o componete é usado no html ele sofre algumas alterações
// O padão camelo é alterado para o seguite padrão: PrimeiroComp = <primeiro-comp />
// Porém o nome do componente támbém pode ser usadao: <PrimeiroComp />
// Cabe ao programdor escolher qual estilo usar para os componentes
// Outra propriedadde muito importante de um componte é o método data()
// Nessa proprieadade você irá retornar um objeto que irá conter as poroprieades do componte
// Essas propriedades podem ser acessadas no template do comp usando chaves duplas {{ data }}
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