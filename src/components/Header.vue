<template>
  <div class="header">
    <h3>Qoutes Added</h3>
    <div class="progress">
      <div class="progress">
        <div
          class="progress-bar"
          :style="{width: (qoutesCount / maxQoutes) * 100 + '%'}"
          v-show="qoutesCount>0"
        >{{qoutesCount}} / {{maxQoutes}}</div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: ["qoutesCount", "maxQoutes"]
};
</script>

<style scoped>
.header {
  width: 95vw;
  padding-bottom: 20px;
  border-bottom: 1px solid rgb(21, 21, 21);
  margin: auto;
}
.progress {
  width: 80vw;
  height: 30px;
}
.progress-bar {
  background: linear-gradient(
    264deg,
    rgba(2, 0, 36, 1) 0%,
    rgba(203, 205, 69, 1) 0%,
    rgba(0, 212, 255, 1) 100%
  );
  height: 30px;
  border-radius: 4px;
  transition: ease all 0.5s;
}
</style>


