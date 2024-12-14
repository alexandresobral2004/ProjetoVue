<template>
  <div class="componente bg-light">
    <h1>Componente com Dados Reativos Primitivos</h1>
    <p>Nome:{{nome}} | Idade:{{idade}}</p>
    
    <button @click="incrementar">Incrementar Idade</button>
    <button v-on:click="decrementar">Decrementar Idade</button>
    <button @click="mudarNome">Novo Nome</button>
    
  </div>
</template>

<script setup>
// o script setup serve para deixar o componente reativo
//o ref serve para deixar o componente reativo
import { ref } from 'vue';

const idade = ref(20);
const nome = ref('Matheus');

const incrementar = () => {
  idade.value++;
};

const decrementar = () => {
  idade.value--;
};

const mudarNome = () => {
  nome.value = 'Mariana';
};

const mudarNome2 = () => {
  nome.value = 'Angélica';
};
</script>
