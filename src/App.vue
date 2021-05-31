<template>
  <div class="container">
    <quote-grid :quotes="quote"></quote-grid>
  </div>
</template>

<script>


import QuoteGrid from './components/QuoteGrid.vue'
export default {
  
  name: 'App',
  components:{
    QuoteGrid
    
  },
  data(){
    return{
      quote: [{
        message:'Just a quote to see something'
      },
      {
        message:'Deutschland uber alles'
      },
      {
        message:'Deutschland uber alles'
      },
      {
        message:'Deutschland uber alles'
      },
      ],
      
       
      
      maxQuote: 10,
    }
  }
 
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
