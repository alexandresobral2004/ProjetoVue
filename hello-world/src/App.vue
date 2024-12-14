<script setup>


// import Formulario from './components/formulario.vue';
import IncrementaValor from './components/IncrementaValorPrimitivos.vue';
import IncrementaValorNaoPrimitivo from './components/IncrementaValorNaoPrimitivo.vue';
import DataBinding from './components/DataBinding.vue';
import ComProps from './components/ComProps.vue';
import EscutaEvento from './components/EscutaEvento.vue';

// export default {
//   name: 'App',
//   components: {
//     // Formulario,
//     IncrementaValor,
//     IncrementaValorNaoPrimitivo,
//     DataBinding,
//     ComProps

//   }
// }
</script>


<template>
<div>
    <!-- <Formulario /> -->
 <IncrementaValor />
  <IncrementaValorNaoPrimitivo />
  <DataBinding />
  <!-- v-bind faz o valor ser interpretado como number, podemos usar o atalho :valor   -->
  <ComProps item="Notebook" :valor="1000"/>
  <ComProps item="Caneta" :valor="10.00"/>

  <EscutaEvento />
</div>
</template>