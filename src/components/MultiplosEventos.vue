<template>
    <div>
        <button @click="primeiro($event), segundo(txt2, $event), terceiro()">Ativar Múltiplos Elementos</button>
        <p>{{multiplos_eventos}}</p>
    </div>
</template>

<script>
    export default{
        name: 'MultiplosEventos',
        data(){
            return{
                multiplos_eventos:"",
                txt2: "segundo Evento!"
            }
        },
        methods:{
            primeiro(e){
                this.multiplos_eventos = "Primeiro evento ativado!"
            },
            segundo(txt,e){
                setTimeout(() => this.multiplos_eventos = txt,1000)
            },
            terceiro(){
                setTimeout(() => this.multiplos_eventos = "",2000)
            }
        }
    }
</script>

<style scoped>
    div{
        margin: 100px;
    }
</style>