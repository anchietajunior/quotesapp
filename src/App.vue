<template>
  <div id="app" class="container">
    <h1>Quotes app</h1>
    <app-header :quoteCount="quotes.length" :maxQuotes="maxQuotes"></app-header>
    <app-new-quote @quoteAdded="newQuote"></app-new-quote>
    <quotes-grid v-bind:quotes="quotes" @quoteDeleted="deleteQuote"></quotes-grid>
    <div class="row app-info">
      <div class="col-lg-12 text-center">
        <div class="alert alert-info">To delete a quote, click it!</div>
      </div>    
    </div>
  </div>
</template>

<script>
import Header from './components/Header.vue'
import NewQuote from './components/NewQuote.vue'
import QuotesGrid from './components/QuotesGrid.vue'

export default {
  name: 'app',
  components: {
    appNewQuote: NewQuote,
    QuotesGrid,
    appHeader: Header
  },
  methods: {
    newQuote(quote) {
      this.quotes.push(quote)
    },
    deleteQuote(index) {
      this.quotes.splice(index, 1)
    }
  },
  data() {
    return {
      quotes: [
        'First quote',
        'Second quote'
        ],
      maxQuotes: 10
    }
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

.app-info {
  margin-top: 40px;
}
</style>
