<template>
  <div class="tooltip" :class="bg_color">
    <slot></slot>
  </div>
</template>

<script>
export default {
  name: "MyTip",
  props: {
    bg_color: {
      type: String,
      default: 'light'
    }
  }
}
</script>

<style lang="less" scoped>
.tooltip {
  position: relative;
  width: 40px;
  height: 14px;
  padding: 10px;
  margin: 10px;
  border: solid #000000 1px;
  border-radius: 6px;
  text-align: center;
  font-size: 12px;
  line-height: 1.2;
  word-wrap: break-word;
}
.tooltip:after {
  content: "";
  position: absolute;
  top: 31px;
  left: 13px;
  width: 6px;
  height: 6px;
  border-right: 1px solid black;
  border-bottom: 1px solid black;
  background-color: #fff;
  transform: rotate(45deg);
}

.light {
  background-color: #ffffff;
  &:after {
    background-color: #ffffff;
  }
}

.dark {
  background-color: #000000;
  color: white;
  &:after {
    background-color: #000000;
  }
}
</style>