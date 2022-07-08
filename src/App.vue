<template>
  <div>
    <PrimeiroComponente />
    <OutroComponente />
    <p>O Dado de App é: {{ testando }}</p>
    <LifeCycle />
  </div>
</template>


<script>

  import PrimeiroComponente from './components/PrimeiroComponente.vue'
  import OutroComponente from './components/OutroComponente.vue'
  import LifeCycle from './components/LifeCycle.vue'

  export default{
    name:'App',
    components: {
      PrimeiroComponente,
      OutroComponente,
      LifeCycle
    },
    data(){
      return{
        testando: "Teste"
      }
    }
    
  }
</script>