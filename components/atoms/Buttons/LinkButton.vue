<template>
  <div>
    <a :href="href">{{ text }}</a>
  </div>
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
  width: 100%;
  color: white;
  text-decoration: none;
}
</style>