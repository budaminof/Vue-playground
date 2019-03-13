<template>
  <div class="quote">
    <slot name="title">opsi, something went wrong</slot>
  </div>
</template>

<script>
export default {
  props: ["quotes"]
};
</script>

<style scoped>
.quote {
  width: 400px;
  border: 1px solid rgb(21, 21, 21);
  text-align: center;
  margin: 10px;
}
</style>


