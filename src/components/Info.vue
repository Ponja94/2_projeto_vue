<template>
    <div>
        <Picture />

        <p v-if = "esta_trabalhando">Estou trabalhando no momento.</p>
        <p v-else>Em busca de novas oportunidades</p>
        <p>Utilizo as seguintes tecnologias para back-end:</p>
        <ul>
            <li v-for="(technology, index) in backend_technologies" v-bind:key="index">{{technology}}</li>
        </ul>
        <p>Utilizo as seguintes tecnologias para front-end:</p>
        <ul>
            <li v-for="technology in frontend_technologies" :key="technology.id"> {{technology.language}}</li>
        </ul>
        <h1 class="teste" v-if=" 3 > 2 ">Olá mundo, verdadeiro</h1>
        <div>
            <button @click="showEmail">{{texto_botao}}</button>
        </div>
        <p v-show="mostrar_email">Mande uma mensagem para: {{email}}</p>
        <p>Para meu portfólio basta <a v-bind:href="meu_link" target="_blank">clicar aqui!</a></p>
    </div>
</template>

<script>
    import { throwStatement } from '@babel/types'
import Picture from './Picture.vue'

    export default{
        name: 'Info',
        components:{
            Picture
        },
        props:{
            email: String,
            esta_trabalhando: Boolean
        },
        data(){
            return{
                mostrar_email: false,
                meu_link: 'https://google.com',
                texto_botao:"Mostrar e-mail",
                backend_technologies: ['Javascript', 'PHP', 'Python', 'Django'],
                frontend_technologies: [
                    {id: 1, language:'HTML'},
                    {id: 2, language: 'CSS'},
                    {id: 3, language: 'Vue'}
                ]
            }
        },
        methods: {
            showEmail(){
                this.mostrar_email = !this.mostrar_email
                if(!this.mostrar_email){
                    this.texto_botao = "Mostrar e-mail"
                } else{
                    this.texto_botao = "Esconder e-mail"
                }
            }
        }
    }
</script>

<style>
    .teste{
        color: blue;
    }
</style>