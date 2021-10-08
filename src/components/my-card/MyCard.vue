<template>
  <div class="card" :class="bg_color"></div>
</template>

<script>
export default {
  name: "MyCard",
  props: {
    bg_color: {
      default: 'light',
      type: String
    }
  }
}
</script>

<style lang="less" scoped>
@card_color: #1e1e1e;
.card {
  width: 100px;
  height: 100px;
  border-radius: 5px;
  border: 1px solid black;
  box-shadow: 2px 2px 0 0 gray;
}
.light {
  background: white;
}
.dark {
  background: @card_color;
}
</style>