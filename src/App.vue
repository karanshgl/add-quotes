<template>
<div class="container">
  <new-quote></new-quote>
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
    }

}
</script>

<style>

</style>
