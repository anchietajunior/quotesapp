<template>
  <ul class="list-group">
    <li class="list-group-item" v-for="(quote, index) in quotes" :key="index" @click="deleteQuote(index)">{{ quote }}</li>
  </ul>
</template>

<script>

export default {
  name: 'QuotesGrid',
  props: ['quotes'],
  methods: {
    deleteQuote(index) {
      this.$emit('quoteDeleted', index)
    }
  }
}
</script>

<style scoped>

</style>
