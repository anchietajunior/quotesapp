<template>
  <div class="row header">
    <div class="col-lg-12">
      <div class="progress">
        <div class="progress-bar" role="progressbar" aria-valuenow="60" aria-valuemin="0" aria-valuemax="100"
          :style="{width: (quoteCount / maxQuotes) * 100 + '%'}">
          {{ quoteCount }} / {{ maxQuotes }}
        </div>
      </div>
    </div>
  </div>  
</template>

<script>
export default {
  props: ['quoteCount', 'maxQuotes']
}
</script>

<style scoped>
.header {
  margin: 30px 0;
}
</style>
