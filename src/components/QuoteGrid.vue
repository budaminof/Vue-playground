<template>
  <div class="row">
    <app-quote v-for="(quote, i) in quotes" :key="i" @click.native="deleteQoute(i)">
      <template v-slot:title>
        <h1>{{quote}}</h1>
      </template>
    </app-quote>
  </div>
</template>

<script>
import Quote from "./Quote.vue";
export default {
  components: { appQuote: Quote },
  props: ["quotes"],
  methods: {
    deleteQoute(i) {
      this.$emit("quoteDeleted", i);
    }
  }
};
</script>

<style scoped>
</style>

// @click.native =>
// app-quote is not in the DOM of this components
// by using native you tell it to pretent like it did happen in the DOM of this component

