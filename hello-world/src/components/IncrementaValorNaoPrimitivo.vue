<template>
    <div class="componente">
        <h1>Componente Com Dados Reativos Não Primitivos</h1>
        <p>Nome: {{ pessoa.nome }} | Idade: {{ pessoa.idade }}</p>
        <button @click="fazerAniversario">Fazer Aniversário</button>
        <button @click="mudarNome()">Mudar Nome</button>

        <div class="bg-light">
            <p>Nome: {{ pessoa.nome }} | Idade: {{ pessoa.idade }}</p>
        </div>
    </div>
</template>

<script>
//Formato usando composition API, mudar o script para setup
// import { reactive } from 'vue';
// const pessoa = reactive({
//     nome:"Ana",
//     idade:27
// });
// function fazerAniversario(){
//     pessoa.idade++;
// }

// function mudarNome(){
//     pessoa.nome = 'Mariana';
// }


//formato usando option API
export default {
    data() {
        return {
            pessoa: {
                nome:"Ana",
                idade:27
            }
        };
    },
    methods: {
        fazerAniversario:function(){
            this.pessoa.idade++;
        },
        mudarNome:function(){
            this.pessoa.nome = 'Mariana';
        }
    }
}
</script>

