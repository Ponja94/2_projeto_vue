<template>
  <div>
    <Header />
    <PrimeiroComponente />
    <OutroComponente />
    <p class="gerando">O Dado de App é: {{ testando }}</p>
    <LifeCycle />
    <Pessoa />
  </div>
</template>


<script>
  import Header from './components/Header.vue'
  import PrimeiroComponente from './components/PrimeiroComponente.vue'
  import OutroComponente from './components/OutroComponente.vue'
  import LifeCycle from './components/LifeCycle.vue'
  import Pessoa from './components/Pessoa.vue'

  export default{
    name:'App',
    components: {
      Header,
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

<style>

  body{
   background-color: #333;
   color: #fff 
  }

  .gerando{
    color: black;
    background-color: #fff;
  }

</style>