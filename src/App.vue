<template>
  <div>
    <PrimeiroComponente />
    <OutroComponente />
    <p>O Dado de App é: {{ testando }}</p>
    <LifeCycle />
    <Pessoa />
  </div>
</template>


<script>

  import PrimeiroComponente from './components/PrimeiroComponente.vue'
  import OutroComponente from './components/OutroComponente.vue'
  import LifeCycle from './components/LifeCycle.vue'
  import Pessoa from './components/Pessoa.vue'

  export default{
    name:'App',
    components: {
      PrimeiroComponente,
      OutroComponente,
      LifeCycle,
      Pessoa,
    },
    data(){
      return{
        testando: "Teste"
      }
    }
    
  }
</script>