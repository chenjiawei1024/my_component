<template>
  <button class="button"><span class="success"></span></button>
</template>

<script>
export default {
  name: "MySuccess",
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
  background: #f3f3f3;
  border-radius: 12px;
  box-shadow: #cecece 0 9px;
  border: 0;
  display: inline-block;
  transition: 0.2s ease-in;
  margin-top: 18px;
  margin-left: 9px;
}
.success {
  width: 10px;
  height: 10px;
  transform: rotate(225deg);
  background: #cecece;
  top: 15px;
  left: 33px;
  position: relative;
  display: flex;
  transition: 0.2s ease-in;
}
.success:before {
  content: '';
  width: 100%;
  height: 500%;
  background: inherit;
  position: absolute;
}
.success:after {
  content: '';
  width: 300%;
  height: 100%;
  background: inherit;
  position: absolute;
}
.button:hover > .success {
  background: #5cb85c;
}
.button:active {
  background: #5cb85c;
  box-shadow: #1c7430 0 2px 0 0;
  transform: translateY(7px);
}
.button:active > .success {
  background: white;
}
</style>