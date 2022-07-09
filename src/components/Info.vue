<template>
    <div>
        <Picture />
        <p v-if = "esta_trabalhando">Estou trabalhando no momento.</p>
        <p v-else>Em busca de novas oportunidades</p>
        <p>Utilizo as seguintes tecnologias:</p>
        <ul>
            <li>JavaScript</li>
            <li>PHP</li>
            <li>Python</li>
        </ul>
        <h1 v-if=" 3 > 2 ">Olá mundo, verdadeiro</h1>
        <p v-show="mostrar_email">Mande uma mensagem para: {{email}}</p>
        <p>Para meu portfólio basta <a v-bind:href="meu_link" target="_blank">clicar aqui!</a></p>
    </div>
</template>

<script>
    import Picture from './Picture.vue'

    export default{
        name: 'Info',
        components:{
            Picture
        },
        data(){
            return{
                esta_trabalhando: false,
                mostrar_email: true,
                email: 'henrique.danielb@gmail.com',
                meu_link: 'https://google.com'
            }
        }
    }
</script>