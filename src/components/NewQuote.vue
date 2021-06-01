<template>
  <div class="row">
    <div class="col-md-10 adder">
      <form action="">
        <label for="">Quote</label>
        <textarea
          class="form-control"
          name=""
          id=""
          rows="3"
          v-model="quote"
        ></textarea>

        <div>
          <button class="btn btn-primary quote-btn" @click.prevent="createNew">
            Add Quote
          </button>
        </div>
      </form>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      quote: "",
    };
  },

  methods: {
    createNew() {
      this.$emit("quoteAdded", this.quote);
      this.quote = "";
    },
  },
};
</script>

<style scoped>
.adder {
  margin: 15px;
  padding: 25px;
}
.quote-btn {
  margin-top: 15px;
}
</style>
