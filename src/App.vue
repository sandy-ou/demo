<template>
  <div id="app">
    <div v-for="comp in currentView" :key="comp">
      <component :is="comp"/>
    </div>
  </div>
</template>

<script>
import Components from './components'

export default {
  name: 'app',
  components: Components,
  created(){
    //view components get from backend services
    let currViewComps = ['ComponentA', 'ComponentB', 'ComponentC'];

    this.currentView = currViewComps;
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
