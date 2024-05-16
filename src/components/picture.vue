<template>
    <div>
        <img :src="avatar" v-bind:alt="descricao">
        <mudarimagem @trocar-imagem="trocarImagem" />
    </div>

</template>
<script>

import mudarimagem from './mudarImagem.vue'

export default {
    nome:'Pic',
    data(){
        return{
            avatar: '/img/avatar.png',
            descricao: 'Victor Hugo'

        }
    },
    components:{
        mudarimagem
    },
    methods:{
        trocarImagem(){
            if(this.avatar === '/img/avatar.png'){
                this.avatar = '/img/avatar2.png'
            }
            else if(this.avatar === '/img/avatar2.png'){
                this.avatar = '/img/avatar.png'
            }

        }
    }
}

</script>


((não é necessario por o v-bind, colocando apenas os ':' como uma sintaxe resumida ))