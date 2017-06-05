<template>
<div class="container">
  <app-header :quoteCount="quotes.length" :maxQuotes="maxQuotes"></app-header>
  <new-quote @addQuote="newQuote"></new-quote>
  <quote-grid :quotes="quotes" @quoteDeleted="deleteQuote"></quote-grid>
  <div class="col-sm-12 text-center">
    <div class="alert alert-info">Info : Click on the quote to delete it </div>
  </div>
</div>

</template>

<script>
import QuoteGrid from './components/QuoteGrid.vue';
import NewQuote from './components/NewQuote.vue';
import Header from './components/Header.vue';

export default {
  data:function(){
    return {
        quotes: ['Hello'],
        maxQuotes: 10,
    }},
    components:{
      quoteGrid: QuoteGrid,
      newQuote: NewQuote,
      appHeader : Header
    },
    methods:{
      newQuote(data){
        if(this.quotes.length>=this.maxQuotes){
          return alert('Please delete quote first');
        }
        this.quotes.push(data);

      },
      deleteQuote(i){
        this.quotes.splice(i,1);
      }
    }

}
</script>

<style>

</style>
