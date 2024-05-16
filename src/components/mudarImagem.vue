<template>
    <div>
        <button @click="$emit('trocarImagem')">Trocar imagem de perfil</button>
    </div>
</template>

<script>
//import Pic from './picture.vue'

export default {
    name: 'mudarimagem',
    emits: ['trocarImagem']

}
</script>

