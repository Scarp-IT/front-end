<template>
    <main>
        <div class="home"></div>
        <div class="servicos"></div>
        <div class="scarpidia"></div>
        <div class="contato"></div>
    </main>
</template>

<script setup lang="ts">
    import Menu from "./components/Menu.vue";
</script>

<style lang="scss" scoped>

    main{
        width: 100vw;
        height: 100%;
        background: linear-gradient(180deg, #1B0073 5.73%, #8365F4 100%);
    }

    main > div{
        width: 100%;
        height: 100vh;
    }

    main > div:first-child{
        // background-color: rgba(255, 255, 255, 0.143);
    }

</style>
