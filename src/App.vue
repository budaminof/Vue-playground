<template>
  <div class="container">
    <app-header :qoutesCount="quotes.length" :maxQoutes="maxQoutes"></app-header>
    <app-new-quotes @quoteAdded="newQuote"></app-new-quotes>
    <app-quote-grid :quotes="quotes" @quoteDeleted="removeQoute"></app-quote-grid>
    <div class="info-box">
      <p>Info: click on a quote to delete it</p>
    </div>
  </div>
</template>

<script>
import QuoteGrid from "./components/QuoteGrid.vue";
import NewQuote from "./components/NewQuotes.vue";
import Header from "./components/Header.vue";
export default {
  components: {
    appQuoteGrid: QuoteGrid,
    appNewQuotes: NewQuote,
    appHeader: Header
  },
  data: function() {
    return {
      quotes: [
        "Be the change you wish to see in the world",
        "Curiosity killed the cat",
        "Rome wasn’t built in a day"
      ],
      maxQoutes: 10
    };
  },
  methods: {
    newQuote(quote) {
      if (this.quotes.length >= this.maxQoutes) {
        alert("Please remove qoutes first");
      } else {
        this.quotes.push(quote);
      }
    },
    removeQoute(i) {
      this.quotes.splice(i, 1);
    }
  }
};
</script>

<style>
body {
  font-family: "Oswald", sans-serif;
  color: rgb(21, 21, 21);
}
.info-box {
  position: absolute;
  bottom: 10px;
  z-index: 10;
  height: 50px;
  width: 100vw;
  background-color: white;
}
</style>
