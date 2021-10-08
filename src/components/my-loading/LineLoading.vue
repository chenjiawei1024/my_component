<template>
  <div class="box">
    <div class="line"></div>
    <div class="line"></div>
    <div class="line"></div>
    <div class="line"></div>
  </div>
</template>

<script>
export default {
  name: "MyLoading"
}
</script>

<style lang="less" scoped>
@font_color: #c7c7c7;
.box {
  display: flex;
  justify-content: center;
  align-items: center;
  width: 100px;
  height: 100px;
  border-radius: 10px;
  background: @font_color;
  opacity: 0.5;
  position: fixed;
  left: 50%;
  top: 40%;
  z-index: 999;
}
.line {
  display: flex;
  height: 20px;
  width: 4px;
  background: rgb(2, 90, 108);
  margin-right: 4px;
  margin-top: 6px;
  border-radius: 6px;
  animation: line-bounce 1s infinite ease-in-out;

  &:nth-child(1) {animation-delay: 0s;}
  &:nth-child(2) {animation-delay: 0.2s;}
  &:nth-child(3) {animation-delay: 0.3s;}
  &:nth-child(4) {animation-delay: 0.4s;}
}
@keyframes line-bounce {
  0% { transform: scale(1);}
  20% { transform: scale(1,2);}
  40% { transform: scale(1);}
}
</style>