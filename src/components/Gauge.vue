<template>
  <div>
    <div class="chart-skills">
      <div class="progress">
        <div class="progress-spot"></div>
      </div>
      <div class="needle"></div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {};
  }
};
</script>

<style scoped lang="stylus">
.chart-skills *,
.chart-skills::before
  box-sizing border-box
  width: z

.chart-skills
  position relative
  width 400px
  height 200px
  overflow hidden
  padding 1vh 0


.chart-skills::before,
.chart-skills::after
  position absolute

.chart-skills::before
  content ''
  width inherit
  height inherit
  border 12px solid rgba(211, 211, 211, .3)
  border-bottom none
  border-top-left-radius 200px
  border-top-right-radius 200px
  top 2vh


.progress
  position absolute
  top 100%
  left 0
  width inherit
  height inherit
  border 10px solid
  border-top none
  border-bottom-left-radius 200px
  border-bottom-right-radius 200px
  transform-origin 50% 0
  transform-style preserve-3d
  backface-visibility hidden
  animation-fill-mode forwards
  animation-duration 1.9s
  animation-name rotate-one
  animation-timing-function linear

  .progress-spot
    width 27px
    height 27px
    z-index 5
    position absolute
    border-radius 50%
    background-color black
    left -15px
    top -2px

.needle
    width 13px
    height 106px
    background #999999
    border-bottom-left-radius 5px
    border-bottom-right-radius 5px
    border-top-left-radius 100%
    border-top-right-radius 100%
    display inline-block
    left 180px
    position absolute
    bottom 7px
    animation move 1.9s linear
    transform rotate(70deg)
    transform-origin bottom


@keyframes rotate-one
  100%
    transform rotate(160deg)

@keyframes move
    0%
        transform:rotate(-90deg)
    100%
        transform:rotate(70deg)
</style>
