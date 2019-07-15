<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <Rule RuleExpression="This is the Rule Expression"/>
  </div>
</template>

<script>
//import HelloWorld from './components/HelloWorld.vue'
import Rule from './components/Rule.vue'

export default {
  name: 'app',
  components: {
    //HelloWorld,
    Rule
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
