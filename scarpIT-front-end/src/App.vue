<template>
    <main>
        <div id="home">
            <Menu></Menu>
            <div id="frase">
                <h1>Scarp.IT</h1>
                <h1>Scarp.IT</h1>
                <p id="sub">Seus Guadiões Digitais ;)</p>
                <img src="./assets/easterEgg.svg" alt="">
            </div>
        </div>
        <img id="bg" src="./assets/BGsvg.svg" alt="">
        <div id="servicos"></div>
        <div id="scarpidia"></div>
        <div id="contato"></div>
    </main>
</template>

<script setup lang="ts">
    import Menu from "./components/Menu.vue";
</script>

<style lang="scss" scoped>

    @font-face {
        font-family: 'Jet Brains';
        src: url('./assets/fonts/JetBrainsMono-Regular.ttf') format('truetype');
        font-weight: normal;
    }

    @font-face {
        font-family: 'Jet Brains-Bold';
        src: url('./assets/fonts/JetBrainsMono-Bold.ttf') format('truetype');
        font-weight: bold;
    }

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

    #home{
        padding-top: 35px;
        display: grid;
        justify-content: center;
    }

    #frase{
        font-family: 'Jet Brains-Bold';
        font-weight: bold;
        z-index: 10;

        h1:first-child{
            top: 40.5%;
            left: 50.5%;
            color: #8365F4;
        }
        
        *{
            position: absolute;
            font-size: 140px;
            top: 40%;
            left: 50%;
            transform: translate(-50%, -50%);
            color: #fff;
        }

        p{
            font-family: 'Jet Brains';
            font-size: 36px;
            top: 62%;
            left: 50%;
            transform: translate(-50%, -50%);
        }

        img{
            left: 82%;
            top: 60%;
            width: 6rem;
        }
    }

    #bg{
        position: absolute;
        width: 100vw;
        top: 70%;
        left: 50%;
        transform: translate(-50%, -50%);
        filter: blur(0.5px);
        z-index: 9;
    }
    

</style>
