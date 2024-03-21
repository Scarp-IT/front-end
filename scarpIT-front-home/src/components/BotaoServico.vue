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
        position: relative;
        align-items: center;
        width: 224px;
        height: 296px;
        border-radius: 5px;
        background: rgba(0, 0, 0, 0.07);
        box-shadow: 4px 4px 4px 0px rgba(0, 0, 0, 0.25);
        backdrop-filter: blur(5px);
        -webkit-backdrop-filter: blur(5px);
        z-index: 10;
        overflow: hidden;
        cursor: pointer;
        
        @media screen and (max-width: 1024px) {
            height: 200px;
        }

        img{
            width: 90%;
            object-fit: contain;

            @media screen and (max-width: 1024px) {
                width: auto;
                height: 100%;
                opacity: 0.5;
                top: 20%;
                transform: translateY(-10%);
            }
        }

        h1{
            position: absolute;
            top: 10rem;
            justify-self: center;
            font-family: system-ui, -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
            font-weight: 200;
            font-size: 3rem;

            @media screen and (max-width: 1024px) {
                width: 100%;
                font-size: 5vw;
                top: 7rem
            }
        }
    }
</style>