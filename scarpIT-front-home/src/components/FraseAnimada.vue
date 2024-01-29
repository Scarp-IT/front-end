<template>
    <div class="typewriter">
        <h1><strong>Com a Scarp It,</strong></h1>
        <p ref="animado" style="opacity: 0;">{{frase[Math.floor(Math.random() * 4)]}}</p>
    </div>
</template>

<script setup lang="ts">
    import { ref, onMounted } from 'vue';
    
    const frase1 = 'você detecta problemas antes deles afetarem seus clientes...';
    const frase2 = 'você garante a confiabilidade de seus sistemas na nuvem...';
    const frase3 = 'você otimiza a eficiência operacional, proporcionando um APM de alto desempenho...';
    const frase4 = 'você está sempre um passo à frente em termos de gerenciamento de nuvem e SRE...';
    const frase = ref([frase1, frase2, frase3, frase4]);
    const animado = ref();

    const observer = new IntersectionObserver((entries, observer) => {
        entries.forEach((entry) => {
            if(entry.isIntersecting){
                animado.value.style.opacity = 1;
                animado.value.classList.add('animated');
                observer.unobserve(entry.target);
            }
        })
    })

    onMounted(() => {
        observer.observe(animado.value);
    });

</script>
<style lang="scss" scoped>
    /* GLOBAL STYLES */
    body {
        background: #333;
        padding-top: 5em;
        display: flex;
        justify-content: center;
    }

    /* DEMO-SPECIFIC STYLES */
    .typewriter {
        h1 {
            color: #fff;
            font-size: 2.5rem;
            font-family: system-ui, -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
            overflow: hidden; /* Ensures the content is not revealed until the animation */
            white-space: nowrap; /* Keeps the content on a single line */
            margin: 0 auto; /* Gives that scrolling effect as the typing happens */
            letter-spacing: 0; /* Adjust as needed */
            text-transform: uppercase;
        }

        p {
            padding-top: 10px;
            color: #fff;
            font-size: 1.2rem;
            font-family: system-ui, -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
            overflow: hidden; /* Ensures the content is not revealed until the animation */
            border-right: .15em solid orange; /* The typwriter cursor */
            white-space: nowrap; /* Keeps the content on a single line */
            margin: 0 auto; /* Gives that scrolling effect as the typing happens */
            letter-spacing: 0; /* Adjust as needed */
            text-transform: uppercase;
        }

        @media screen and (max-width: 1024px) {
            h1{
                font-size: 1.7rem;
            }

            p{
                font-size: .8rem;
                white-space: initial;
                padding: 20px 50px;
                border-right: none;
            }
        }
    }

    .animated{
        animation: 
        typing 3.5s steps(40, end),
        blink-caret .5s step-end infinite;

        @media screen and (max-width: 1024px){
                -webkit-animation: puff-in-center 0.7s cubic-bezier(0.470, 0.000, 0.745, 0.715) both;
                animation: puff-in-center 0.7s cubic-bezier(0.470, 0.000, 0.745, 0.715) both;
        }
    }

    /* The typing effect */
    @keyframes typing {
        from { width: 0 }
        to { width: 100% }
    }

    /* The typewriter cursor effect */
    @keyframes blink-caret {
        from, to { border-color: transparent }
        50% { border-color: #8365F4 }
    }


    @-webkit-keyframes puff-in-center {
        0% {
            -webkit-transform: scale(2);
                    transform: scale(2);
            -webkit-filter: blur(4px);
                    filter: blur(4px);
            opacity: 0;
        }
        100% {
            -webkit-transform: scale(1);
                    transform: scale(1);
            -webkit-filter: blur(0px);
                    filter: blur(0px);
            opacity: 1;
        }
        }
        @keyframes puff-in-center {
        0% {
            -webkit-transform: scale(2);
                    transform: scale(2);
            -webkit-filter: blur(4px);
                    filter: blur(4px);
            opacity: 0;
        }
        100% {
            -webkit-transform: scale(1);
                    transform: scale(1);
            -webkit-filter: blur(0px);
                    filter: blur(0px);
            opacity: 1;
        }
    }


</style>