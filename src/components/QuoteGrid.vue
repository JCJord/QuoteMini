<template>
  <div class="row">
    <the-quote
      v-for="(quote, index) in quotes"
      :key="quote.message"
      @click.native="deleteQuote(index)"
    >
      {{ quote.message }}
    </the-quote>
  </div>
</template>

<script>
import TheQuote from "./TheQuote.vue";

export default {
  props: ["quotes"],
  components: {
    TheQuote,
  },

  methods: {
    deleteQuote(index) {
      this.$emit("quoteDeleted", index);
    },
  },
};
</script>

<style></style>
