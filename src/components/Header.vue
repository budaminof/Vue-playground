<template>
  <div class="header">
    <h3>Qoutes Added</h3>
    <div class="progress">
      <div class="progress">
        <div
          class="progress-bar"
          :style="{width: (qoutesCount / maxQoutes) * 100 + '%'}"
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
  width: 80vw;
}
.progress {
  width: 80vw;
  height: 30px;
}
.progress-bar {
  background-color: green;
  height: 30px;
}
</style>


