<template>
  <div class="row">
    <form>
      <div>
        <label>Quote</label>
        <textarea row="3" v-model="quote"></textarea>
      </div>
      <div>
        <button @click.prevent="createNew">ADD NEW QUOTE</button>
      </div>
    </form>
  </div>
</template>

<script>
export default {
  data: function() {
    return {
      quote: ""
    };
  },
  methods: {
    createNew() {
      this.$emit("quoteAdded", this.quote);
      this.quote = "";
    }
  }
};
</script>

<style scoped>
</style>


