<template>
    <div>
        <MudarPicture @mudar-imagem="trocarImagem"/>
        <img :src="avatar" :alt="descricao">
    </div>
</template>

<script>
import MudarPicture from './MudarPicture.vue';
export default{
    name: "Picture2",
    components:{
        MudarPicture,
    },
    data() {
        return {
            avatar: "/img/avatar-1.png",
            descricao: "Daniel Bellé"
        };
    },
    methods:{
        trocarImagem(){
            this.avatar = "/img/avatar-2.png"
        }
    }
}
</script>