<template>
    <div class="container">
        <div>
            <app-new-quote @quoteAdded="newQuote"></app-new-quote>
            <app-quote-grid :quotes='quotes'></app-quote-grid>
        </div>
    </div>
</template>

<script>
import NewQuote from './components/NewQuote.vue';
import QuoteGrid from './components/QuoteGrid.vue';
    export default {
        data: function(){
            return {
                quotes: [ 'First Quote'
                ],
                maxQuotes: 10
            }
        },
        components: {
            appNewQuote: NewQuote,
            appQuoteGrid: QuoteGrid
        },
        methods: {
            newQuote(quote){
                this.quotes.push(quote);
            }
        }
    }
</script>

<style>
</style>
