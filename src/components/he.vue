<template>
    <div>
        <ul>
            <li ><a href="#">Home</a></li>
            <li><a href="#">Projetos</a></li>
            <li><a href="#">Contato</a></li>
            <li v-if="estaLogado"><a href="#">Meu perfil</a></li>
        </ul>
    </div>
    
</template>

<script>
export default {
    name: 'he',
    //uma forma de passar props por array (não é possivel tipar o dado)
    props: ['estaLogado']
}
</script>

<style scoped>
ul {
    list-style: none;
    display: flex;
    background: #111;
    
}
li{
    padding: 10px;
}
</style>
