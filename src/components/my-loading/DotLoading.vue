<template>
  <div class="box">
    <div class="dots1"></div>
    <div class="dots2"></div>
    <div class="dots3"></div>
  </div>
</template>

<script>
export default {
  name: "DotLoading"
}
</script>

<style lang="less" scoped>
@font_color: #c7c7c7;
.box {
  display: flex;
  align-items: center;
  justify-content: center;
  width: 100px;
  height: 100px;
  position: fixed;
  left: 50%;
  top: 40%;
  border-radius: 10px;
  background: @font_color;
  opacity: 0.5;
  z-index: 999;
}
.dots1 {
  width: 16px;
  height: 16px;
  position: absolute;
  right: 20px;
  border-radius: 50%;
  background: rgb(2, 90, 108);
  opacity: 0.2;
  animation: dot-left 1s infinite linear;
}
.dots2 {
  width: 16px;
  height: 16px;
  position: relative;
  border-radius: 50%;
  background: rgb(2, 90, 108);
  opacity: 0.6;
  animation: dot-middle 1s infinite linear;
}
.dots3 {
  width: 16px;
  height: 16px;
  position: absolute;
  left: 20px;
  border-radius: 50%;
  background: rgb(2, 90, 108);
  opacity: 1;
  animation: dot-right 1s infinite linear;
}
@keyframes dot-left {
  0% { opacity: 0.2; }
  25% { opacity: 0.6; }
  50% { opacity: 1; }
  75% { opacity: 0.6; }
  100% { opacity: 0.2; }
}
@keyframes dot-middle {
  0% { opacity: 0.6; }
  25% { opacity: 1; }
  50% { opacity: 0.6; }
  75% { opacity: 0.2; }
  100% { opacity: 0.6; }
}
@keyframes dot-right {
  0% { opacity: 1; }
  25% { opacity: 0.6; }
  50% { opacity: 0.2; }
  75% { opacity: 0.6; }
  100% { opacity: 1; }
}
</style>