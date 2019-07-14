<template>
  <div class="hello">
    <h1>{{ RuleName }}</h1>
    <p>
     Welcome, to the new age AI bused Rule editor and interpretor.
     You can type up a business rule in common English language and the rules behind the scenes
     will get interpreted in machine language, stored and executed as needed.
    </p>
     <div>{{ RuleExpression }}</div>
  </div>
 
</template>


<script>
import axios from 'axios';
export default {
  name: 'Rule',
  props: {
    RuleExpression: String
  },
   data() {
    return {};
  },
  mounted() {
    axios.get("https://jsonplaceholder.typicode.com/todos/")
  }
}


</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>