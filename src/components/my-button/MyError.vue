<template>
  <button class="button"><span class="error"></span></button>
</template>
<!--1.为什么transition没有被渲染-->
<!--2.为什么按钮顶部会有空隙-->
<script>
export default {
  name: "MyError",
  props: {
    size: {
      default: 'middle'
    }
  }
}
</script>

<style lang="less" scoped>
* {
  padding: 0;
  margin: 0;
}
.button {
  width: 90px;
  height: 75px;
  border-radius: 12px;
  background: #f3f3f3;
  border: 0;
  box-shadow: #cecece 0 9px;
  margin-left: 9px;
  margin-top: 18px;
  transition: 0.2s ease-in;
}
.error {
  position: relative;
  left: 22px;
  display: flex;
  align-items: center;
  background: #cecece;
  transition: 0.2s ease-in;
}
.error:before,
.error:after{
  content: "";
  background: #cecece;
  position: absolute;
  left: 19px;
  width: 10px;
  height: 50px;
  transition: 0.2s ease-in;
}
.button:active {
  transform: translateY(7px);
  box-shadow: darkred 0 2px;
  background: #f56c6c;
}
.error:before {
  transform: rotate(45deg);
}
.error:after {
  transform: rotate(-45deg);
}
.button:hover > .error:before,
.button:hover > .error:after {
  background: #f56c6c;
}
.button:active > .error:before,
.button:active > .error:after {
  background: white;
}
</style>