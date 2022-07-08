<template>
  <div>
    <PrimeiroComponente />
    <OutroComponente />
    <p>O Dado de App é: {{ testando }}</p>
  </div>
</template>


<script>

  import PrimeiroComponente from './components/PrimeiroComponente.vue'
  import OutroComponente from './components/OutroComponente.vue'

  export default{
    name:'App',
    components: {
      PrimeiroComponente,
      OutroComponente
    },
    data(){
      return{
        testando: "Teste"
      }
    }
    
  }
</script>