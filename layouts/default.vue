<template>
    <div>

        <AppHeader />

        <NuxtPage />

        <AppFooter />

    </div>
</template>

<script>

import { AppHeader } from "../components/organisms/Header";
// 名前付きimport
// AppHeader, index.js 同じフォルダで無かったからパスがおかしいと言われた

import { AppFooter } from "../components/organisms/Footer";

export default {
    components: { 
        AppHeader,
        AppFooter
    }
};

</script>

<style lang='scss' scoped>

</style>