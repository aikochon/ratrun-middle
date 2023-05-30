<template>
  <div>
    <div>
      <nav>
        <li v-for="(link, key) in Logo" :key="key">
          <nuxt-link :to="link.to">{{ link.text }}</nuxt-link>
        </li>
      </nav>
    </div>
    <div>
      <nav>
        <li v-for="(link, key) in LinkList" :key="key">
          <nuxt-link :to="link.to">{{ link.text }}</nuxt-link>
        </li>
      </nav>
    </div>
    <div>
      <nav>
        <li v-for="(link, key) in LinkListSecondLine" :key="key">
          <nuxt-link :to="link.to">{{ link.text }}</nuxt-link>
        </li>
      </nav>
    </div>
  </div>
</template>
  
  <script>
export default {
  setup() {
    const Logo = reactive([
      { text: "Logo", to: "#" },
      { text: "Interior & design", to: "#" },
    ]);
    const LinkList = reactive([
      { text: "ホーム", to: "#" },
      { text: "私達について", to: "#" },
      { text: "選ばれる理由", to: "#" },
      { text: "ワークフロー", to: "#" },
      { text: "FAQ", to: "#" },
      { text: "事例紹介", to: "#" },
    ]);
    const LinkListSecondLine = reactive([
      { text: "会社概要", to: "#" },
      { text: "お問合せ・お見積り", to: "#" },
      { text: "個人情報保護法について", to: "#" },
    ]);
    return {
      Logo,
      LinkList,
      LinkListSecondLine,
    };
  },
};
</script>
  
  <style lang='scss' scoped>
div {
  display: flex;
}
nav {
  display: block;
  gap: 20px;
  padding: 30px 20px;
}
li {
  list-style: none;
}
a {
  text-decoration: none;
  color: black;
}
</style>