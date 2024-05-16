<template>
    <div>
        <p>Este é meu segundo componente e minha profissão é: {{ profissao }}</p>
        <form >
            Front-End <input type="radio" placeholder="Front-End" value="Front-End" v-model= "profissao">
            Back-End <input type="radio" placeholder="Back-End" value="Back-End" v-model= "profissao">
            FullStack <input type="radio" placeholder="FullStack" value="FullStack" v-model= "profissao">
        </form>
            
    </div>
</template>

<script>
export default {
    name: 'SegundoComponente',
    data(){
        return{
            profissao: ''
        }
    }
}
</script>
