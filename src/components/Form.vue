<template>
    <div>
        <h2>Meu formulário:</h2>
        <form action="" @submit="enviarFormulario($event)">
            <div>
                <input type="text" v-model="name">
            </div>
            <div>
                <input type="text" v-model="email">
            </div>
            <!--<div>
                <InputText />
            </div> -->
            <div>
                <Submit />
            </div>
        </form>
        <p>Conteudo</p>
        <p>Conteudo</p>
        <p>Conteudo</p>
    </div>
</template>

<script>
import InputText from './form/InputText.vue'
import Submit from './form/Submit.vue'

export default{
    name:'Form',
    data(){
        return {
            name: "",
            email: ""
        }
    },
    components: {
        InputText,
        Submit
    },
    methods:{
        enviarFormulario(e){
            e.preventDefault();

            const name = this.name;
            const email = this.email;

            console.log('form enviado')
            console.log('O nome é: '+ name +" e o email é: "+email)

            // Ajax 
            // Inserir banco de dados
        }
    }
}

</script>

<style scoped>
    p{
        margin: 150px;
    }
</style>