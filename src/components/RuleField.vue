<template>

  <div class="hello">
    <h1>{{ RuleName }}</h1>
    <p>
     In this component, we will submit some rule fields
    </p>
     <div class="row">
     </div>
  </div>
 
</template>


<script>
import axios from 'axios';
export default {
  name: 'RuleField',
  props: {
    RuleName: String
  },
   data() {
    return { rulesfields: [],
      loading: false};
    
  },
  mounted() {
     
  /*  axios.get("https://localhost:44325/api/rules")
    .then(
        
        response => {this.loading = false;this.rules = response.data;  
        console.log('response.data', response.data); }
       
    )
    .catch(error => console.log(error))*/
    
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