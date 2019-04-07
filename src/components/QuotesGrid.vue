<template>
  <ul class="list-group">
    <li class="list-group-item" v-for="quote in quotes" :key="quote.id">{{ quote }}</li>
  </ul>
</template>

<script>

export default {
  name: 'QuotesGrid',
  props: ['quotes']
}
</script>

<style scoped>

</style>
