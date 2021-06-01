<template>
  <div class="prog-container">
    <div class="col-md-10 bar-wrap">
      Current quote: {{ quoteCount }} / {{ maxQuotes }}
      <b-progress :value="quoteCount" :max="10" animated class="prog-bar">
      </b-progress>
    </div>
  </div>
</template>

<script>
export default {
  props: ["quoteCount", "maxQuotes"],
  data() {
    return {};
  },
};
</script>

<style scoped>
.bar-wrap {
  margin-bottom: 20px;
}
.prog-container {
  margin: 10px;
}
</style>
