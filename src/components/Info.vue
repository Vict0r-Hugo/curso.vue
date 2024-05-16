<template>
    <div>
        <h3> Olá, meu Nome é {{ nome }}</h3>
        <div v-if = "estaTrabalhando">
            <p>Estou trabalhando no momento</p>
            <p>De Setembro de 2023 até o momento</p>
        </div>
        <div v-else="estaTrabalhando">
            <p>Estou buscando Oportunidades.</p>
        </div>
        <div>
            <button @click="showEmail">{{ mostrarButton }}</button>
        </div>
        <div v-show = "mostrarEmail">
            <p>{{ email }}</p>
        </div>
        <div>
            <p> Meu portifólio <a v-bind:href="meuLink" target="_blank">Clique</a></p>
            <Pic/>
        </div>
        <div>
            <!--utilizando v-for (É utilizado para exibir dados de um array ou objeto)-->
            <p>Utilizo as seguintes tecnologias para o back-end</p>
            <ul >
                <!--utilizando v-for com array-->
                <li v-for = " (Tec, index) in backEndTecnologies" v-bind:key="index">{{ Tec }} </li>
            </ul>
        </div>
        <div>
            <p>Utilizo as seguintes tecnologias para o Front-end</p>
            <ul >
                <!--utilizando v-for com objeto (v-bind pode ser escrito apenas como :key="Tec.id")-->
                <li v-for = " (Tec) in frontEndtecnologies" v-bind:key="Tec.id">{{ Tec.linguagem }} </li>
            </ul>
        </div>
        <div>
            {{ compEmail }} - {{ email }}
        </div>
    </div>
</template>

<script>
import Pic from './picture.vue'

    export default {
        //exportando
        name: 'Info',
        //props é um recurso para passar dado do componente pai para o componente filho, podendo alterar como cada componente é executado de forma individual.
        props:{
            compEmail: String,
            email: String 
        },
        //data é onde trabalhamos com dados dinamicos
        data(){
            return{
                estaTrabalhando: true,
                mostrarEmail: false,
                nome: 'Victor Hugo',
                meuLink:'https://google.com',
                mostrarButton: 'Mostrar email',
                frontEndtecnologies: [
                    {id: 1, linguagem:'React.js'},
                    {id: 2, linguagem:'Vue.js'},
                    {id: 3, linguagem: 'HTML'}
            ],
                backEndTecnologies: ['Node.Js', 'PHP']
            }
        },
        //instanciando os components importados para a utilização
        components:{
            Pic
        }, 
        //utilizando funções
        methods:{
            showEmail(){
                this.mostrarEmail = !this.mostrarEmail
                if(!this.mostrarEmail){
                    this.mostrarButton = 'Mostrar email'
                }
                else{
                    this.mostrarButton = "Esconder email"
                }
            }
        }
        
    }
   
</script>