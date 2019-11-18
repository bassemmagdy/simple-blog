<template>
  <div class="container">
    <app-header :quoteCount="quotes.length" :maxQuotes="maxQuotes"></app-header>
    <new-quote v-on:addQuoteEvent="addQuote($event)"></new-quote>
    <app-quote-grid
      :quotes="quotes"
      v-on:deleteQuote="quotes.splice(i, 1)"
    ></app-quote-grid>
    <div class="row">
      <div class="col-sm-12 text-center">
        <div class="alert alert-info">
          Info: Click on a QUote to Delete
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import QuoteGride from './components/QuoteGride.vue';
import NewQuoteVue from './components/NewQuote.vue';
import HeaderVue from './components/Header.vue';
export default {
  data() {
    return {
      quotes: ['Just a Quote'],
      maxQuotes: 10
    };
  },
  components: {
    appQuoteGrid: QuoteGride,
    newQuote: NewQuoteVue,
    appHeader: HeaderVue
  },
  methods: {
    addQuote($event) {
      console.log(this.quotes.length);
      this.quotes.length < 10
        ? this.quotes.push($event)
        : alert('You hit max volume');
    }
  }
};
</script>

<style></style>
