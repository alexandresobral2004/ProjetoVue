<template>
  <div class="componente">
    <h1>Componente que escuta evento</h1>
    <p>Total:R${{total}}</p>
    <div class="lista">
      <!-- <EmiteEvento item="Item1" :valor="2.00" @adicionar="total+=$event"/>
      <EmiteEvento item="Item2" :valor="3.00" @adicionar="total+=$event"/>
      <EmiteEvento item="Item3" :valor="1.00" @adicionar="total+=$event"/> -->

      <EmiteEvento item="Item1" :valor="2.00" @adicionar="atualizarTotal"/>
      <EmiteEvento item="Item2" :valor="3.00" @adicionar="atualizarTotal"/>
      <EmiteEvento item="Item3" :valor="1.00" @adicionar="atualizarTotal"/>
           
  </div>
</div>

</template>

<script setup>
import EmiteEvento from './EmiteEvento.vue';
import {ref} from 'vue';

const total = ref(0)
function atualizarTotal(p){
  const valor = total.value + p
  total.value = +valor.toFixed(2);

}

</script>

<style scoped>
.lista{
  display: flex;
  justify-content: space-around;
}
</style>