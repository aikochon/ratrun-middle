<template>
  <a :href="href">{{ text }}</a>
</template>
  <script>
export default {
  props: {
    text: { type: String, default: "ボタン" },
    href: { type: String, default: "#" },
  },
  setup() {},
};
</script>
<style lang='scss' scoped>
a {
  background-color: cadetblue;
  color: white;
}
</style>