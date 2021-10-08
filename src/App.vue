<template>
  <div>
    <div class="container">
      <my-favor></my-favor>
      <my-success></my-success>
      <my-error></my-error>
    </div>
<!--      <dot-loading></dot-loading>-->
      <circle-loading></circle-loading>
      <my-card></my-card>
    <my-tip bg_color="dark">hello</my-tip>
  </div>
</template>

<script>
import MyFavor from "./components/my-button/MyFavor.vue";
import MySuccess from "./components/my-button/MySuccess.vue";
import MyError from "./components/my-button/MyError.vue";
import LineLoading from "./components/my-loading/LineLoading.vue";
import DotLoading from "./components/my-loading/DotLoading.vue";
import CircleLoading from "./components/my-loading/CircleLoading.vue";
import MyCard from "./components/my-card/MyCard.vue";
import MyTip from "./components/my-tooltip/MyTip.vue";

export default {
  name: 'MyApp',
  components: {
    MyTip,
    MyCard,
    CircleLoading,
    DotLoading,
    MyError,
    MySuccess,
    MyFavor,
    LineLoading
  },
}
</script>
<style lang="less">
.container {
  display: flex;
}
</style>
