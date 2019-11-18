<template>
  <div class="row">
    <form action="">
      <div
        class="col-sm8 cols-offset-2 col-xs-12 col-md-6 col-md-offset-3 form-group"
      >
        <label for="">Quote</label>
        <textarea class="form-control" rows="3" v-model="quote"></textarea>
      </div>
      <div
        class="col-sm8 cols-offset-2 col-xs-12 col-md-6 col-md-offset-3 form-group"
      >
        <button class="btn btn-primary" @click.prevent="createNew">
          Add Quote
        </button>
      </div>
    </form>
  </div>
</template>

<script>
import Quote from './Quote.vue';
export default {
  data() {
    return {
      quote: ''
    };
  },
  methods: {
    createNew() {
      this.$emit('addQuoteEvent', this.quote);
      this.quote = '';
    }
  }
};
</script>
<style></style>
