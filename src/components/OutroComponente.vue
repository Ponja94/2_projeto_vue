<template>
    <div>
        <h1>Olá Outro Componente!</h1>
        <p>Meu nome é {{ nome }} e trabalha como {{ profissao }}</p>    
    </div>
    
</template>

<script>
    export default {
        name: 'OutroComponente',
        data(){
            return {
                nome: "Daniel",
                profissao: "Programador"
            }
        }
    }
</script>