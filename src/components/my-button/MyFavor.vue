<template>
  <button class="button"><span class="heart"></span></button>
</template>

<script>
export default {
  name: "MyFavor",
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
.button:active {
  background: #ec4989;
  box-shadow: #a12355 0 2px 0 0;
  transform: translateY(7px);
}
.heart {
  width: 24px;
  height: 24px;
  transform: rotate(45deg);
  background: #cecece;
  top: 5px;
  left: 33px;
  position: relative;
  display: flex;
  transition: 0.2s ease-in;
}
.heart:before,
.heart:after {
  content: "";
  width: 100%;
  height: 100%;
  border-radius: 50%;
  background: inherit;
  position: absolute;
}
.button:hover > .heart {
  background: #ec4989;
}
.button:active > .heart {
  background: white;
}
.heart:before {
  left: -50%;
}
.heart:after {
  top: -50%;
}

</style>