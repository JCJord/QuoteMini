<template>
  <div class="wrapper">
    <the-heading></the-heading>
    <div class="container">
      <new-quote @quoteAdded="newQuote"></new-quote
      ><progress-bar
        :maxQuotes="maxQuote"
        :quoteCount="currentQuote"
      ></progress-bar>
      <quote-grid :quotes="quote" @quoteDeleted="deleteQuote"></quote-grid>

      <b-alert show variant="info" class="info-alert text-center col-md-10"
        >Click in the Quote to delete it</b-alert
      >
    </div>
  </div>
</template>

<script>
import NewQuote from "./components/NewQuote.vue";
import QuoteGrid from "./components/QuoteGrid.vue";
import TheHeading from "./components/TheHeading.vue";
import ProgressBar from "./components/ProgressBar.vue";
export default {
  name: "App",
  components: {
    QuoteGrid,
    NewQuote,
    TheHeading,
    ProgressBar,
  },
  data() {
    return {
      quote: [
        {
          message: "Example Quote !",
        },
      ],
      currentQuote: 1,
      maxQuote: 10,
    };
  },
  methods: {
    newQuote(quote) {
      if (quote.length <= 0) {
        alert("Please add at least one character");
        quote.preventDefault();
      } else if (this.currentQuote < 10) {
        this.quote.push({ message: quote });
        this.currentQuote++;
      } else {
        quote.preventDefault;
      }
    },
    deleteQuote(index) {
      this.quote.splice(index, 1);
      this.currentQuote--;
    },
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

.wrapper {
  width: 100%;
  max-width: 100%;
}
.info-alert {
  margin: 20px;
  padding: 20px;
}
</style>
