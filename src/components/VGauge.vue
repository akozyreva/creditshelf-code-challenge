<template>
  <div>
    <v-gauge
      :value="value"
      :initialValue="initialValue"
      :height="height"
      :options="options"
      :maxValue="maxValue"
    />
  </div>
</template>

<script>
import VGauge from "vgauge";

export default {
  components: {
    VGauge
  },
  data() {
    return {
      value: 80,
      unit: "ss",
      maxValue: 100,
      height: "80",
      initialValue: 80,
      options: {
        angle: 0,
        lineWidth: 0.13,
        colorStart: "#0000FF",
        pointer: {
          length: 0.4,
          strokeWidth: 0.07,
          color: "#A9A9A9"
        }
      },
      gaugeValueClass: "*"
    };
  }
};
</script>

<style scoped lang="stylus">
* >>> .gauge-title
  display none
</style>
