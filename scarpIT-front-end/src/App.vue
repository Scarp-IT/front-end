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
        <div id="bg">
            <img src="./assets/BGsvg.svg" alt="">
        </div>
        <div id="servicos">
            <div id="frase-animada">
                <FraseAnimada></FraseAnimada>
            </div>
            <div id="botoes-servicos" style="padding-top: 4rem;">
                <BotaoServico :img="imgSre" titulo="SRE" @click="mudarServico('sre')"></BotaoServico>
                <BotaoServico :img="imgNuvem" titulo="Nuvem" @click="mudarServico('nuvem')"></BotaoServico>
                <BotaoServico :img="imgApm" titulo="APM" @click="mudarServico('apm')"></BotaoServico>
            </div>
            <div ref="servicoDescricao" id="servico-descricao">
                <div id="servico-img">
                    <img :src="servicoImg" alt="" >
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
                <div id="principal" @click="clickBtnBlk('http://wiki.scarpit.tech/performance/democratiza%C3%A7%C3%A3o')">
                    <div class="img-principal">
                        <img src="./assets/jmeter.webp" alt="">
                    </div>
                    <h2><strong>JMeter</strong></h2>
                    <p>Potencialize o desempenho da sua aplicação com insights precisos. Descubra como com nosso guia sobre JMeter.</p>
                </div>
                <div id="svg-divisao">
                    <svg xmlns="http://www.w3.org/2000/svg" width="12" height="100%" viewBox="0 0 12 549" fill="none">
                    <path d="M6 0.666667C3.05448 0.666667 0.666667 3.05448 0.666667 6C0.666667 8.94552 3.05448 11.3333 6 11.3333C8.94552 11.3333 11.3333 8.94552 11.3333 6C11.3333 3.05448 8.94552 0.666667 6 0.666667ZM5 6L5 594H7L7 6H5Z" fill="white" fill-opacity="0.3"/>
                    </svg>
                </div>
                <div id="secundaria">
                    <div id="um" @click="clickBtnBlk('http://wiki.scarpit.tech/cyber-security')">
                        <img src="./assets/cybersecurity.jpeg" alt=""/>
                        <div>
                            <h2><strong>Cyber Security</strong></h2>
                            <p>Preocupado sobre sua segurança cibernéticas? Nosso documento sobre segurança cibernética é essencial para sua defesa online.</p>
                        </div>
                    </div>
                    <div id="dois" @click="clickBtnBlk('http://wiki.scarpit.tech/observabilidade')">
                        <img src="./assets/observabilidade.png" alt=""/>
                        <div>
                            <h2>Observabilidade</h2>
                            <p>Descubra um novo horizonte de insights... <br/>Explore nosso documento sobre Observabilidade agora!</p>
                        </div>
                    </div>
                </div>
                <div id="botao-up" @click="clickBtnScroll('home')">
                    <div id="">
                        <svg xmlns="http://www.w3.org/2000/svg" width="38" height="35" viewBox="0 0 38 35" fill="none">
                            <path d="M20.7678 1.23199C19.7915 0.25568 18.2085 0.25568 17.2322 1.23199L1.32233 17.1419C0.346019 18.1182 0.346019 19.7011 1.32233 20.6774C2.29864 21.6537 3.88155 21.6537 4.85786 20.6774L19 6.53529L33.1421 20.6774C34.1184 21.6537 35.7014 21.6537 36.6777 20.6774C37.654 19.7011 37.654 18.1182 36.6777 17.1419L20.7678 1.23199ZM21.5 35L21.5 2.99976L16.5 2.99976L16.5 35L21.5 35Z" fill="white" fill-opacity="0.3"/>
                        </svg>
                        <span>UP</span>
                    </div>
                </div>
            </div>
        </div>
        <div id="contato">
            <div id="formulario">
                <h1>Sua aplicação 24/7.</h1>
                <p>Deixe-nos ajudar você a alcançar e manter um ambiente altamente disponível e robusto. Se você escapar para as montanhas e sem sinal, estaremos aqui, cuidando para que tudo funcione perfeitamente.</p>
                <!-- <div id="inputs">
                    <input type="text" placeholder="Nome" v-model="objFormulario.Nome">
                    <input type="text" placeholder="Email" v-model="objFormulario.Email">
                    <textarea name="assunto" id="txa-assunt" v-model="objFormulario.Assunto" cols="auto" rows="4" placeholder="Assunto"></textarea>
                    <button @click="enviarForm()">Enviar ✈️</button>
                </div> -->
            </div>
            <div id="info">
                <h1>Info</h1>
                <div id="email">
                    <img src="./assets/iconEmail.svg" alt="iconMail" @click="clickBtnBlk('mailto:scarpit@scarpit.tech')">
                    <p>scarpit@scarpit.tech</p>
                </div>
                <div id="phone">
                    <img src="./assets/iconPhone.svg" alt="iconePhone" @click="clickBtnBlk('tel:+5513991486248')">
                    <p>+55 13 99148-6248</p>
                </div>
                <div id="social">
                    <img src="./assets/Insta.svg" alt="instagram" @click="clickBtnBlk('https://www.instagram.com/scarpit.tech/')">
                    <img src="./assets/Linkedin.svg" alt="linkedin" @click="clickBtnBlk('https://www.linkedin.com/company/scarp-it-technology-consulting/')">
                    <img src="./assets/Github.svg" alt="github" @click="clickBtnBlk('https://github.com/Scarp-IT')">
                </div>
            </div>
            <div id="bg-down">
                <img src="./assets/BGsvgDown.svg" alt="">
            </div>
        </div>
    </main>
</template>

<script setup lang="ts">
    import { ref, onMounted } from 'vue';
    //@ts-expect-error
    import service from './service/service';
    
    import Menu from "./components/Menu.vue";
    import BotaoServico from "./components/BotaoServico.vue";
    import FraseAnimada from "./components/FraseAnimada.vue";

    import imgSre from './assets/sre.png';
    import imgNuvem from './assets/nuvem.png';
    import imgApm from './assets/apm.png';

    // const imgSre = '/assets/sre.png';
    // const imgNuvem = '/assets/nuvem.png';
    // const imgApm = '/assets/apm.png';

    const servicoTitulo = ref('');
    const servicoFrase = ref('');
    const servicoImg = ref();

    // const emailEnviado = ref(false);

    const servicoDescricao = ref();
    const onServicoDescricao = ref(false);

    // let objFormulario = reactive({Nome: '', Email: '', Assunto: ''});

    onMounted(() => {

    });

    function clickBtnBlk(url: string){
        window.open(url, '_blank');
    };

    function clickBtnScroll(url: string){
        //@ts-expect-error
        document.getElementById(url).scrollIntoView({ behavior: 'smooth' });
    };

    function mudarServico(tipo: string){
        onServicoDescricao.value = true;
        servicoDescricao.value.classList.remove('scale-in-top');
        servicoDescricao.value.classList.add('scale-in-top');

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
    };

    // async function enviarForm() {};

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
        overflow: hidden;
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
            font-size: 10rem;
            top: 40%;
            left: 50%;
            transform: translate(-50%, -50%);
            color: #fff;

            @media screen and (max-width: 1024px) {
                font-size: 15vw;
            }
        }

        p{
            font-family: 'Jet Brains';
            font-size: 30px;
            top: 70vh;
            left: 50%;
            transform: translate(-50%, -50%);
            @media screen and (max-width: 1024px) {
                top: 60vh;
            }
        }

        img{
            left: 82%;
            top: 60%;
            width: 6rem;
        }
    }

    #bg{
        position: relative;
        width: 100vw;
        height: 0;

        img{
            position: absolute;
            width: 110vw;
            top: 70%;
            left: 50%;
            transform: translate(-50%, -50%);
            filter: blur(0.5px);
            z-index: 1;

            @media screen and (max-width: 1024px) {
                width: 150%;
                top: -200px;
            }
        }

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
            gap: 20px;
        }
    }

    #servico-descricao{
        display: flex;
        width: 70vw;

        @media screen and (max-width: 1024px) {
            flex-direction: column;       

            :first-child > img{
                position: absolute;
                top: 80%;
                left: 50%;
                transform: translate(-50%, -50%);
                opacity: 0.3;
                width: 100%;
            }
        }

        > div {
            flex: 1 1 50%;
        }

        img{
            width: 130%;
            opacity: 0.4;
        }

        #servico-info{
            display: flex;
            flex-direction: column;
            justify-content: center;
            z-index: 12;
            font-family: 'Jet Brains-Bold';
            opacity: .8;

            h1{
                font-size: 6rem;
                margin-bottom: 0;
            }
            
            p {
                font-size: 1.1rem;
            };

            @media screen and (max-width: 1024px) {
                h1{
                    font-size: 4rem;
                }

                p{
                    font-size: 0.8rem;
                }
            }
        }
    }

    #scarpidia{
        display: flex;
        align-items: center;
        flex-direction: column;
        width: 100vw;
        height: 100%;
        font-family: 'Jet Brains-Bold';
        padding-bottom: 8rem;

        img {
            opacity: 0.9;
        }

        @media screen and (max-width: 1024px) {
            padding-top: 10vh;
        }

        #scarpidia-titulo{
            width: 70%;
            height: 20%;
            font-size: 1.6rem;

            h1{
                margin: 0;
            }

            @media screen and (max-width: 1024px) {
                font-size: 4vw;
            }
        }

        #scarpidia-grid{
            width: 100%;
            height: 80%;
            display: flex;
            justify-content: center;
            position: relative;

            > div{
                width: 35%;
            }

            #principal{
                display: flex;
                flex-direction: column;
                align-items: center;
                height: 100%;
                padding-right: 3vw;
                padding-top: 4rem;
                text-align: initial;

                > *{
                    width: 100%;
                    margin: 0;
                    cursor: pointer;
                }

                .img-principal{
                    display: flex;
                    height: 60%;
                    border-radius: 5px;
                    overflow: hidden;

                    img{
                        width: 100%;
                        object-fit: cover;
                    }
                }

                h2{
                    padding: 0.6rem 0;
                }
            }

            #secundaria{
                height: 100%;
                padding-left: 3vw;
                padding-top: 4rem;
                display: flex;
                flex-direction: column;
                gap: 2.5rem;

                > div{
                    height: 40%;
                    display: flex;
                    gap: 1rem;
                    cursor: pointer;
                    
                    :nth-child(1){
                        width: 40%;
                        border-radius: 5px;
                        object-fit: cover;
                    }

                    :nth-child(2){
                        width: 60%;
                        text-align: initial;
                        display: flex;
                        flex-direction: column;
                        gap: 1rem;
                        
                        > *{
                            width: 100%;
                            margin: 0;
                        } 

                        p{
                            font-size: 0.9rem;
                        }

                    }


                }
            }

            #svg-divisao{
                width: 0;
                position: relative;
                svg{
                    position: absolute;
                    top: 3.5rem;
                    left: -.3rem;
                }
            }

            #botao-up{
                display: flex;
                position: absolute;
                width: 10%;
                aspect-ratio: 4/1.7;
                top: calc(100% + 3.5rem);
                border: 1px solid #ADA4CD;
                justify-content: center;
                align-items: center;
                cursor: pointer;

                span{
                    opacity: .3;
                    font-weight: 900;
                }
            }

            @media screen and (max-width: 1024px) {
                flex-direction: column;
                align-items: center;

                > div:not(#botao-up){
                    width: 70%;
                    padding: 3vh 0 !important;
                }
                #svg-divisao{
                    display: none;
                }
                #botao-up{
                    padding: 1rem;
                    top: calc(100% + 1rem);
                }
                #principal{
                    p{
                        font-size: 2.8vw;
                    }
                }
                #secundaria{
                    height: 50vh;
                    h2{
                        font-size: 4vw;
                    }
                    p {
                        font-size: min(2.4vw, 1rem) !important;
                    }

                }
            }
        }

    }

    #contato{
        display: flex;
        align-items: center;
        justify-content: center;
        width: 100vw;
        height: 100%;
        font-family: 'Jet Brains-Bold';
        padding-bottom: 9rem;
        overflow: hidden;

        
        > div:not(#bg-down){
            width: 35%;
        }
        
        @media screen and (max-width: 1024px){
            flex-direction: column;
            padding-top: 10vh;
            > div:not(#bg-down){
                width: 60%;
            }
        }

        #formulario{
            text-align: initial;
            padding-right: 3vw;
            z-index: 10;

            h1{
                font-size: 2.5rem;
            }

            @media screen and (max-width:1024px) {
                padding: 0;
            }

            input, textarea{
                background-color: transparent;
                width: 100%;
                border: none;
                border-bottom: 3px solid rgba(255, 255, 255, 0.30);
                font-size: 1.3rem;
                outline: none;
                padding-top: 1.5rem;
                padding-bottom: 0.3rem;
                resize: none;
            }

            input::placeholder, textarea::placeholder{
                color: rgba(255, 255, 255, 0.30);
                font-family: 'Jet Brains';
            }

            button{
                width: 100%;
                aspect-ratio: 10/1;
                border-radius: 5px;
                background: rgba(0, 0, 0, 0.40);
                margin-top: 1rem;
                outline: none;

            }
            
            button:hover{
                border: none;
            }
        }

        #info{
            margin: 0 3vw;
            display: flex;
            flex-direction: column;
            position: relative;
            justify-content: center;
            border-radius: 5px;
            margin-top: 3%;
            background-color: rgba(0, 0, 0, 0.30);
            backdrop-filter: blur(16.5px);
            -webkit-backdrop-filter: blur(16.5px);

            gap: 1rem;
            z-index: 10;
            padding: 4rem 0;

            > *{
                padding: 0 5rem;

                p{
                    overflow-wrap: anywhere;
                    text-align: initial;
                }
            }

            h1{
                text-align: initial;
                margin: 0 0 2rem 0;
            }

            > div{
                display: flex;
                gap: 20px;

                img{
                    cursor: pointer;
                }
            }

            #social{
                position: absolute;
                display: flex;
                flex-direction: column;
                align-self: flex-end;
                right: -150px;
            }

            @media screen and (max-width:1024px) {
                padding: 9vw 0;
                > *:not(#social){
                    padding: 0 9vw;
                }
                
                h1{
                    font-size: min(10vw, 3rem);
                }

                > div:not(#social){
                    flex-direction: column;
                    gap: 0;
                    :first-child{
                        height: 20px;
                        align-self: flex-start;
                    }
                    p{
                        font-size: min(3.4vw ,1.3rem);
                    }
                }
            }
        }
    }

    #bg-down{
        position: relative;
        z-index: 1;
        filter: blur(1px);
        img{
            position: absolute;
            opacity: 50%;
            height: 70vh;
            left: -50vw;
            top: -5vh;
        }

        @media screen and (max-width:1024px) {
            img{
                top: -36vh;
            }
        }
    }

    .scale-in-top {
	-webkit-animation: scale-in-top 0.5s cubic-bezier(0.250, 0.460, 0.450, 0.940) both;
	        animation: scale-in-top 0.5s cubic-bezier(0.250, 0.460, 0.450, 0.940) both;
    }
    @-webkit-keyframes scale-in-top {
        0% {
            -webkit-transform: scale(0);
                    transform: scale(0);
            -webkit-transform-origin: 50% 0%;
                    transform-origin: 50% 0%;
            opacity: 1;
        }
        100% {
            -webkit-transform: scale(1);
                    transform: scale(1);
            -webkit-transform-origin: 50% 0%;
                    transform-origin: 50% 0%;
            opacity: 1;
        }
        }
        @keyframes scale-in-top {
        0% {
            -webkit-transform: scale(0);
                    transform: scale(0);
            -webkit-transform-origin: 50% 0%;
                    transform-origin: 50% 0%;
            opacity: 1;
        }
        100% {
            -webkit-transform: scale(1);
                    transform: scale(1);
            -webkit-transform-origin: 50% 0%;
                    transform-origin: 50% 0%;
            opacity: 1;
        }
    }


</style>
