<template>
    <div>
        <Reutilizacao />
        <img :src="avatar" :alt="descricao">
        <button @click="trocar_foto($event)" >Trocar Foto!</button>
    </div>
</template>

<script>
import Reutilizacao from './Reutilizacao.vue'
export default{
    name: "Picture",
    data() {
        return {
            avatar: "/img/avatar-1.png",
            descricao: "Daniel Bellé"
        };
    },
    components: { 
        Reutilizacao 
    },
    methods:{
        trocar_foto(e){
            this.avatar = "img/avatar-2.png"
            
        }
    },
}
</script>