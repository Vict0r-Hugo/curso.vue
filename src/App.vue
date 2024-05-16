<template>
   <he :estaLogado="true"/>
  <primeiro-componente />
  <segundo-componente/>
  <LifeCycleHooks/>
  <Fo/>
  <!--<Info/>-->
  <pessoa/>
  </template>
  <script>
import he from './components/he.vue'
import PrimeiroComponente from './components/PrimeiroComponente.vue'
import SegundoComponente from './components/SegundoComponente.vue'
import LifeCycleHooks from './components/LifeCycleHooks.vue'
import Fo from './components/Fo.vue'
import Info from './components/Info.vue'
import Pic from './components/picture.vue'
import pessoa from './components/pessoa.vue'


export default {
  name: 'App',
  components:{ 
    he,
    PrimeiroComponente,
    SegundoComponente,
    LifeCycleHooks,
    Fo, 
    Info, 
    Pic,
    pessoa
  }
  }
</script>
<style>
body{
  background-color: #333;
  color: #fff;
}
</style>