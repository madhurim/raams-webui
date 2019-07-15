<template>
  <div class="hello">
    <h1>{{ RuleExpression }}</h1>
    <p>
     Welcome, to the new age AI based Rule editor and interpretor.
     You can type up a business rule in common English language and the rules behind the scenes
     will get interpreted in machine language, stored and executed as needed.
    </p>
     <div class="row">
          <div v-for="rule in rules" :key="rule.RuleId">
          <div class="col-md-4 cards">
             
            <div>
              <h3>{{ rule.RuleId }}</h3>
              <p>{{ rule.RuleName }}</p>
              <p>{{ rule.RuleStatement }}</p>
            </div>
          </div>
        </div>
        </div>
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
    return { rules: [],
      loading: false};
    
  },
  mounted() {
     
    axios.get("https://localhost:44325/api/rules")
    .then(
        
        response => {this.loading = false;this.rules = response.data;  alert(response.data); }
       
    )
    .catch(error => console.log(error))
    
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
.cards {
  background: #F5F5F5;
  height:400px;
}
 .cards:hover {
  transform: translateY(-0.5em);
  background: #EBEBEB;
}


.cards {
   column-count: 1;
  column-gap: 1em;
    margin-top: 70px;

} 
</style>