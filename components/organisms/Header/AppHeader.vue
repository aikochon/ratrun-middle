<template>
  <div class="header-box">
    <div>
      <nav>
        <li v-for="(link, key) in LinkList" :key="key">
          <nuxt-link :to="link.to">{{ link.text }}</nuxt-link>
        </li>
      </nav>
    </div>
    <div class="aboutus-area">
      <div class="aboutus-title">
        <p>理念の文章が入ります</p>
      </div>
      <div class="aboutus-detail">
        <p>
          母体が内装解体専門業者であるからこそ、一般的な施工会社よりも解体費用を抑えることができます。
          つまり、解体費用を抑えることで、余力のある資金が生まれ、使い道を広げることができるということです。<br />
          選択のできる予算の使途も合わせてご提案いたします。
        </p>
      </div>
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
.header-box {
  background-color: darkslateblue;
  color: white;
}
.aboutus-area {
  width: 400px;
  padding: 50px 100px 200px 0px;
  margin: 0 0 0 auto;
}
.aboutus-title {
  font-size: 30px;
}
nav {
  display: flex;
  gap: 20px;
  padding: 30px 20px;
}
li {
  list-style: none;
}
a {
  text-decoration: none;
  color: white;
}
</style>