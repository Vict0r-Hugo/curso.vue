<template>
    <div>
        <h1>Olá Vue</h1>
        <p>Este é o meu primeiro componente em vue.js</p>
        <p>E meu nome é: {{ nome }}</p>
        <input type="text" v-model="nome">
    </div>
    <div>
        <multiplosEventos/>
    </div>
</template>
<script>
import multiplosEventos from './multiplosEventos.vue'
export default {
    name: 'PrimeiroComponente',
    data() {
        return{
            nome: 'Victor'
        }
    }, components:{
        multiplosEventos
    }
}
</script>
