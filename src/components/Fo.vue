<template>
    <div>
        <h1>Cadastre-se</h1>
        <!--O @submit é um envento que chama uma função, geralmente utilizado junto com o preventDefault() para evitar a atualização da pagina -->
        <form action="" @submit="enviarFormulario($event)">
            <!--O v-model recebe o input e insere no componente instanciado no data-->
            <input type="text" v-model="name">
            <input type="text" v-model="email">
            
            <Sub/>
        </form>
        
    </div>
</template>

<script>
    import In from './Form/In.vue'
    import Sub from './Form/Sub.vue'
    
    export default {
        name: 'Fo',
        data(){
            return{
                email:'',
                name:''
            }
        },
        components: {
            In,
            Sub
        },
        methods:{
            enviarFormulario(e){
                e.preventDefault()

                const name = this.name
                const email = this.email

                console.log('passo aqui')
                console.log(name)
                console.log(email)
                

            }
        }
    }
</script>