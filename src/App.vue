<template>
<div class="container">
  <app-header :quoteCount="quotes.length" :maxQuote="maxQuote"></app-header>
  <app-new-quote @quoteAdded="newQuote"></app-new-quote>
  <app-quote-grid :quotes="quotes" @quoteDeleted='deleteQuote'></app-quote-grid>
  <div class="row">
    <div class="col-sm-12 text-center">
      <div class="alert alert-info">
            Info:Click On Quote To Delete It !
      </div>
    </div>
  </div>
</div>

</template>

<script>
import QuoteGrid from './components/QuoteGrid.vue';
import NewQuote from './components/NewQuote.vue';
import Header from './components/Header.vue';



export default {
data(){
  return {
    quotes:[
            'Just A Quote See Something !',
      ],
    maxQuote:10
  }
},
methods:{
  newQuote(quote){
    if(this.quotes.length >= this.maxQuote){
      return alert('Please Delete Quotes First !');
    }
    this.quotes.push(quote);
  },
  deleteQuote(index){
    
    this.quotes.splice(index,1);
  }
},
components:{
  appQuoteGrid:QuoteGrid,
  appNewQuote:NewQuote,
  appHeader:Header,
}
}
</script>

<style scoped>

</style>
