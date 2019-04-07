<template>
  <div class="row">
    <div class="col-lg-12">
      <form>
        <div class="form-group">
          <textarea rows="3" class="form-control" v-model="quote"></textarea>
        </div>
        <div class="form-group">
          <button class="btn btn-primary" @click.prevent="AddNewQuote">Add quote</button>
        </div>
      </form>
    </div>
  </div>
</template>

<script>

export default {
  name: 'NewQuote',
  data() {
    return {
      quote: ''
    }
  },
  methods: {
    AddNewQuote() {
      this.$emit('quoteAdded', this.quote);
      this.quote = ''
    }
  }
}
</script>

<style scoped>

</style>
