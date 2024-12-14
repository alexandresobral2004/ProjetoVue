<template>

  <div class="componente bg-light text-dark">
    <!--oneway databinding-->
    <!-- <input type="text" v-bind:value="valor"> -->
      <!--twoway databinding - Altera a variável com o valor digitado -->
     <!-- <input type="text" v-bind:value="valor" v-on:input="(e) => valor = e.target.value"> <br> -->
      <!-- twoway databinding - Altera a variável com o valor digitado usando v-model-->
       <input type="text" v-model="valor" > 
     <p>{{ valor }}</p>
  </div>
</template>

<script setup>
//composition API

import { ref } from 'vue';//usado para variaveis primitivas
import { reactive } from 'vue';//usado para variaveis nao primitivas

const valor = ref("Vue é muito legal");

</script>

