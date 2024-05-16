<template>
    <div>
            <button @click="primeiro($event), segundo(txt2, $event), terceiro(txt3, $event)">Ativar eventos multiplos</button>
            <p>{{ multiplosEventos }}</p>
    </div>
</template>

<script>
export default {
    name: 'multiplosEventos',
    data(){
        return{
            multiplosEventos: "",
            txt2: 'Segundo evento ativado',
            txt3: 'terceiro evento ativado'
        }
    }, 
    methods:{
        primeiro(e){
            this.multiplosEventos = 'primeiro evento ativado'
        }, 
        segundo(txt2,e){
            setTimeout(() => {
            this.multiplosEventos = txt2
            },2000)
            
        },
        terceiro(txt3,e){
            setTimeout(() => {
                this.multiplosEventos = txt3
            },4000)
            
        }
    }
}
</script>
<style scoped>
div {
    padding: 100px;
}
</style>