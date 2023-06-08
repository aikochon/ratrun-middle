<template>
  <div>
    <AppHeader />

    <NuxtPage />

    <AppFooter />
  </div>
</template>

<script>
import { AppFooter } from "../components/organisms/Footer";
import { AppHeader } from "../components/organisms/Header";

export default {
  components: {
    AppHeader,
    AppFooter,
  },
};
</script>

<style lang='scss' scoped>
</style>