<template>
    <H1>Meu Segundo nome é {{ nome }}</H1>
</template>
    
<script>
    //Lifecyclehooks é utilizado para atualizar um dado de forma programada 
    export default {
        name: 'LifeCycleHooks',
        data(){
            return{
                nome: 'Em desenvolvimento'
            }
        }, 
        created(){
           setTimeout(() => {
                this.nome = 'Victor'
           },5000)
            
        },
        mounted(){
            setTimeout(() => {
                this.nome = 'Hugo'
           },2000)
            
        }
    }




</script>