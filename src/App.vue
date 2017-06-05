<template>
<div class="container">
  <new-quote @addQuote="newQuote"></new-quote>
  <quote-grid :quotes="quotes"></quote-grid>
</div>
</template>

<script>
import QuoteGrid from './components/QuoteGrid.vue';
import NewQuote from './components/NewQuote.vue';

export default {
  data:function(){
    return {
        quotes: ['Hello'],
        maxQuotes: 10
    }},
    components:{
      quoteGrid: QuoteGrid,
      newQuote: NewQuote
    },
    methods:{
      newQuote(data){
        this.quotes.push(data);
      }
    }

}
</script>

<style>

</style>
