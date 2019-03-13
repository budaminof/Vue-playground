<template>
  <div class="new">
    <form>
      <div class="form-elements">
        <h2>Quote</h2>
        <textarea row="3" v-model="quote"></textarea>
        <button @click.prevent="createNew" :disabled="!quote.length">add new qoute</button>
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
.new {
  margin: auto;
  width: 60vw;
}

.form-elements {
  display: flex;
  flex-direction: column;
  text-align: center;
  justify-content: center;
}

textarea {
  font-size: 25px;
  font-family: "Oswald", sans-serif;
}

button {
  width: 250px;
  margin: auto;
  margin-top: 30px;
  height: 50px;
  font-size: 15px;
  text-transform: uppercase;
  font-weight: bold;
  background: rgba(0, 212, 255, 1);
  border-radius: 2px;
  outline: none;
  letter-spacing: 3px;
}
button:disabled {
  background: rgba(0, 213, 255, 0.475);
}
</style>


