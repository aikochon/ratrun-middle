<template>
    <div>

        <AppHeader />

        <NuxtPage />

        <p>フッタ-</p>

    </div>
</template>

<script>

import { AppHeader } from "../components/organisms/Header";

export default {
    components: { 
        AppHeader
    }
};

</script>

<style lang='scss' scoped>

</style>