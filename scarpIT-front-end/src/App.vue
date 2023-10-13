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
        <div id="servicos">
            <div id="frase-animada">
                <FraseAnimada></FraseAnimada>
            </div>
            <div id="botoes-servicos" style="padding-top: 4rem;">
                <BotaoServico :img="imgSre" titulo="SRE" @click="mudarServico('sre')"></BotaoServico>
                <BotaoServico :img="imgNuvem" titulo="Nuvem" @click="mudarServico('nuvem')"></BotaoServico>
                <BotaoServico :img="imgApm" titulo="APM" @click="mudarServico('apm')"></BotaoServico>
            </div>
            <div id="servico-descricao">
                <div id="servico-img">
                    <img :src="servicoImg" alt="" style="opacity: 0.4;">
                </div>
                <div id="servico-info" style="text-align: initial;">
                    <h1>{{ servicoTitulo }}</h1>
                    <p>{{ servicoFrase }}</p>
                </div>
            </div>
        </div>
        <div id="scarpidia">
            <div id="scarpidia-titulo">
                <h1>ScarPidia</h1>
            </div>
            <div id="scarpidia-grid">
                <div id="principal">
                    <div class="img-principal">
                        <img src="./assets/vuebg.png" alt="">
                    </div>
                    <h2>Primeira aplicação em VUE3</h2>
                    <p>Veja como é fácil criar uma aplicação simples com o VUE3.</p>
                </div>
                <div id="svg-divisao">
                    <svg xmlns="http://www.w3.org/2000/svg" width="12" height="434" viewBox="0 0 12 434" fill="none">
                        <path d="M6 0.666667C3.05448 0.666666 0.666667 3.05448 0.666667 6C0.666666 8.94552 3.05448 11.3333 6 11.3333C8.94552 11.3333 11.3333 8.94552 11.3333 6C11.3333 3.05448 8.94552 0.666667 6 0.666667ZM5 6L4.99998 434L6.99998 434L7 6L5 6Z" fill="white" fill-opacity="0.3"/>
                    </svg>
                </div>
                <div id="secundaria"></div>
            </div>
        </div>
        <div id="contato"></div>
    </main>
</template>

<script setup lang="ts">
    import { ref } from 'vue';

    import Menu from "./components/Menu.vue";
    import BotaoServico from "./components/BotaoServico.vue";
    import FraseAnimada from "./components/FraseAnimada.vue"

    import imgSre from './assets/sre.png';
    import imgNuvem from './assets/nuvem.png';
    import imgApm from './assets/apm.png';

    const servicoTitulo = ref('');
    const servicoFrase = ref('');
    const servicoImg = ref(imgNuvem);


    function mudarServico(tipo: string){
        switch(tipo){
            case 'sre':
                {
                    servicoImg.value = imgSre;
                    servicoTitulo.value = 'SRE';
                    servicoFrase.value = 'Nossa expertise em Site Reliability Engineering (SRE) permite que suas operações digitais ocorram sem problemas. Com abordagens nativas e de código aberto, oferecemos soluções para aprimorar a observabilidade, aprimorar a resiliência e promover a melhoria contínua. Trabalhamos nos bastidores para que você possa se destacar na vanguarda.';
                    break;
                };

            case 'nuvem':
                {
                    servicoImg.value = imgNuvem;
                    servicoTitulo.value = 'NUVEM';
                    servicoFrase.value = 'Mergulhe no mundo da tecnologia em nuvem com confiança. Nossos especialistas em nuvem estão preparados para criar e implementar soluções modernas e bem estruturadas. Seja adotando uma abordagem multi-nuvem, híbrida ou migrando completamente, estamos aqui para transformar sua jornada para a nuvem em uma experiência tranquila e eficiente.';
                    break;
                };

            case 'apm':
                {
                    servicoImg.value = imgApm;
                    servicoTitulo.value = 'APM';
                    servicoFrase.value = 'O desempenho do aplicativo é essencial para o sucesso nos negócios digitais. Nossos serviços de Application Performance Management (APM) oferecem testes de desempenho meticulosos, otimizações avançadas e solução de problemas abrangente. Acelere seus aplicativos, minimize gargalos e proporcione uma experiência excepcional aos usuários finais.';
                    break;
                };
        }
    }

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
        z-index: 1;
    }

    #servicos{
        display: flex;
        position: relative;
        height: 100%;
        flex-direction: column;
        align-items: center;
        z-index: 10;

        #botoes-servicos{
            display: flex;
            width: 70%;
            justify-content: space-between;
        }
    }

    #servico-descricao{
        display: flex;
        width: 70vw;

        > div {
            flex: 1 1 50%;
        }

        img{
            width: 130%;
        }

        #servico-info{
            display: flex;
            flex-direction: column;
            justify-content: center;
            z-index: 12;
            font-family: 'Jet Brains-Bold';

            h1{
                font-size: 6rem;
                margin-bottom: 0;
            }
            
            p {
                font-size: 1.1rem;
            };
        }
    }

    #scarpidia{
        display: flex;
        align-items: center;
        flex-direction: column;
        width: 100vw;
        height: 80vh;
        font-family: 'Jet Brains-Bold';

        #scarpidia-titulo{
            width: 70%;
            height: 20%;
            font-size: 1.6rem;

            h1{
                margin: 0;
            }
        }

        #scarpidia-grid{
            width: 100%;
            height: 80%;
            display: flex;
            justify-content: center;

            > div{
                width: 35%;
            }

            #principal{
                display: flex;
                flex-direction: column;
                align-items: center;
                height: 100%;
                padding-right: 5rem;
                padding-top: 4rem;
                text-align: initial;

                > *{
                    width: 100%;
                    margin: 0;
                }

                .img-principal{
                    height: 60%;
                    border-radius: 5px;
                    overflow: hidden;

                    img{
                        width: 100%;
                    }
                }

                h2{
                    padding: 0.6rem 0;
                }
            }

            #secundaria{
                height: 100%;
                padding-left: 5rem;
                padding-top: 4rem;
            }

            #svg-divisao{
                width: 0;
                position: relative;
                svg{
                    position: absolute;
                    top: 3.5rem;
                }
            }

            
        }

    }
    

</style>
