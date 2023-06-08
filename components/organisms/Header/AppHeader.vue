<template>
  <div>
    <div>
      <nav>
        <li v-for="(link, key) in LinkList" :key="key">
          <nuxt-link :to="link.to">{{ link.text }}</nuxt-link>
        </li>
      </nav>
    </div>
  </div>
</template>
      
      <script>
export default {
  setup() {
    const LinkList = reactive([
      { text: "ホーム", to: "#" },
      { text: "経営理念", to: "#" },
      { text: "事業理念", to: "#" },
      { text: "事業目的", to: "#" },
      { text: "お問合せ", to: "#" },
    ]);
    return { LinkList };
  },
};
</script>
      
  <style lang='scss' scoped>
nav {
  display: flex;
  gap: 20px;
  padding: 30px 20px;
  position: fixed;
  left: 0;
  top: 0;
  z-index: 1;
}
li {
  list-style: none;
}
a {
  text-decoration: none;
  color: white;
}
</style>