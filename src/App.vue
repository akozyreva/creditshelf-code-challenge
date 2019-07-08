<template>
  <div id="app">
    <VGauge />
    <Gauge />
  </div>
</template>

<script>
import VGauge from "./components/VGauge.vue";
import Gauge from "./components/Gauge.vue";

export default {
  name: "app",
  components: {
    VGauge,
    Gauge
  }
};
</script>
<style lang="stylus"></style>
