<template>
    <div>
        <button @click="$emit('mudarImagem')">Trocar a imagem de Perfil!</button>
    </div>
</template>

<script>
export default{
    name: 'MudarPicture',
    emits: ['mudarImagem'],
}
</script>