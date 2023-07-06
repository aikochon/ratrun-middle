<template>
  <div class="flex-box">
    <div class="left-area">
      <img
        src="../../../assets/img/logo-2.png"
        class="company-name"
        alt="Logo"
      />
      <p class="company-name">
        Interior design<br />
        &<br />
        Constraction
      </p>
    </div>
    <div class="link-area">
      <nav>
        <li v-for="(link, key) in LinkList" :key="key">
          <nuxt-link :to="link.to">{{ link.text }}</nuxt-link>
        </li>
      </nav>
    </div>
    <div class="link-area">
      <nav>
        <li v-for="(link, key) in LinkListSecondLine" :key="key">
          <nuxt-link :to="link.to">{{ link.text }}</nuxt-link>
        </li>
      </nav>
    </div>
    <div class="right-area">
      <div class="border-area">
        <p>
          建築・建築デザイン・原状回復・内装解体・建物解体・アスベスト除去工事はSENTIAにお任せください！<br />
          <br />
          株式会社SENTIA<br />
          〒454-0982<br />
          愛知県名古屋市高見1-20-2<br />
          TEL:052-1212-2029
        </p>
      </div>
      <div class="sns-area">
        <nav class="sns-links">
          <li v-for="(link, key) in LinkListSnsLine" :key="key">
            <a :href="link.to">
              <img :src="getImg(link.imgSrc)" alt="" />
            </a>
          </li>
        </nav>
      </div>
    </div>
  </div>
</template>
  
  <script>
export default {
  components: ["nuxt-img"],
  setup() {
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
    const LinkListSnsLine = reactive([
      { text: "facebook", to: "#", imgSrc: "facebook.png" },
      { text: "instagram", to: "#", imgSrc: "instagram.png" },
      { text: "pintarest", to: "#", imgSrc: "pintarest.png" },
    ]);
    const getImg = (file) => {
      return new URL(`../../../assets/img/${file}`, import.meta.url).href;
    };
    return {
      LinkList,
      LinkListSecondLine,
      LinkListSnsLine,
      getImg,
    };
  },
};
</script>
  
  <style lang='scss' scoped>
.flex-box {
  display: flex;
  background-color: gray;
  color: white;
  padding: 20px;
}
.left-area {
  width: 15%;
  padding: 5% 5%;
}
img {
  width: 100%;
}
.left-area p {
  padding-top: 20%;
}
.company-name {
  text-align: center;
  vertical-align: middle;
}
.link-area {
  width: 20%;
  text-align: left;
  padding: 4% 5%;
}
.right-area {
  width: 40%;
  padding: auto 5%;
}
.border-area {
  border: 8px double white;
  width: 400px;
  padding: 20px;
  margin: 40px 0 0 auto;
}
.sns-area {
  color: white;
  display: flex;
}
nav {
  display: block;
  gap: 20px;
  padding: 30px 20px;
}
li {
  list-style: none;
  padding-bottom: 10px;
}
a {
  text-decoration: none;
  color: white;
}
.sns-links {
  display: flex;
  margin: 0 0 0 auto;
}
.sns-links li {
  width: 30px;
}
</style>