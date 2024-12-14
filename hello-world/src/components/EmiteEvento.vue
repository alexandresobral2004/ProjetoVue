<template>
  <div class="componente">
    <h1>Componente que emite evento</h1>
    <p>{{ item }} - (R$ {{ valor.toFixed(2) }})</p>
    <button @click="adicionar">Comprar</button>
  </div>
</template>

<script setup>
import {defineProps,defineEmits} from 'vue';
const props = defineProps({
  item: String,
  valor: Number
});

const emit = defineEmits(['adicionar']);

function adicionar(){
  emit('adicionar',props.valor);
}
</script>