<template>
  <div class="box">
    <div class="circle"></div>
  </div>
</template>

<script>
export default {
  name: "CircleLoading"
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
.circle {
  width: 40px;
  height: 40px;
  border: 6px rgba(2, 90, 108,0.25) solid;
  border-top: 6px rgb(2, 90, 108) solid;
  border-radius: 50%;
  animation: spin-circle 1.1s infinite ease-in-out;
}
@keyframes spin-circle {
  from { transform: rotate(0deg); }
  to { transform: rotate(360deg); }
}

</style>