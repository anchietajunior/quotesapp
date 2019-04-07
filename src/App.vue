<template>
  <div id="app" class="container">
    <h1>Quotes app</h1>
    <app-new-quote @quoteAdded="newQuote"></app-new-quote>
    <quotes-grid v-bind:quotes="quotes"></quotes-grid>
  </div>
</template>

<script>
import NewQuote from './components/NewQuote.vue'
import QuotesGrid from './components/QuotesGrid.vue'

export default {
  name: 'app',
  components: {
    appNewQuote: NewQuote,
    QuotesGrid
  },
  methods: {
    newQuote(quote) {
      this.quotes.push(quote)
    }
  },
  data() {
    return {
      quotes: [
        'First quote',
        'Second quote'
        ]
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
</style>
