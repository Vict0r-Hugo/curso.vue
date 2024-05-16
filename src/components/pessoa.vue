<template>
    <div>
        <h1>Cadastre-se</h1>
        <!--Existem duas formas de mandar um dado via props -->
        <!--setando diretamente como no compEmail ou utilizando o v-bind puxando um valor do data (abreveamos o v-bind com ':')-->
        <info compEmail="victorhugo@gmail.com" :email="email"/>
        
        <form action="" @submit="enviarFormulario($event)">
            <in/>
            <in/>
            <Sub/>
        </form>
        
    </div>
</template>

<script>
    import info from './Info.vue'
    import In from './Form/In.vue'
    import Sub from './Form/Sub.vue'

    
    export default {
        name: 'Pessoa',
        data(){
            return{
                email:'victor@gmail.com',
                name:''
            }
        },
        components: {
            In,
            Sub,
            info
        },
        methods:{
            
        }
    }
</script>