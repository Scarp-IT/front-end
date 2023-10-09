<template>
    <div class="botao-servico">
        <img :src="props.img" alt="">
        <h1>{{ props.titulo }}</h1>
    </div>
</template>
<script setup lang="ts">
    const props = defineProps([
        'img',
        'titulo',
    ]);
</script>
<style lang="scss" scoped>
    .botao-servico{
        display: flex;
        flex-direction: column;
        align-items: center;
        width: 224px;
        height: 296px;
        border-radius: 5px;
        background: rgba(0, 0, 0, 0.07);
        box-shadow: 4px 4px 4px 0px rgba(0, 0, 0, 0.25);
        backdrop-filter: blur(5px);
        z-index: 10;
        cursor: pointer;
        :hover{

        }

        img{
            width: 90%;
            object-fit: contain;
        }

        h1{
            position: absolute;
            top: 10rem;
            justify-self: center;
            font-family: system-ui, -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
            font-weight: 200;
            font-size: 3rem;
        }
    }
</style>