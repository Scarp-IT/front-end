<template>
    <div id="menu">
        <h3 style="font-family: 'Jet Brains';">Scarp.IT</h3>
        <div id="acessos">
            <div id="btn-login" class="btn" @click="clickBtnWiki">
                <h2 style="font-family: 'Jet Brains'; margin: 0;">Área<br/>Logada</h2>
            </div>
            <div id="btn-wiki" class="btn" @click="clickBtnWiki">
                <h2 style="font-family: 'Jet Brains'; margin: 0;">Wiki</h2>
            </div>
        </div>
    </div>
</template>

<script setup lang="ts">
    function clickBtnWiki(){
        window.open('http://wiki.scarpit.tech', '_blank');
    }
</script>


<style lang="scss" scoped>
    #menu{
        display: flex;
        width: 70vw;
        height: 60px;
        border-bottom: 1px solid #ADA4CD;
        justify-content: space-between;
        z-index: 10;
    }

    #acessos{
        display: flex;
    }

    #btn-login{
        line-height: normal;
        font-size: .8rem;
        cursor: wait;
        color: #ada4cd79;
        border: 1px solid #ada4cd79;
    }

    .btn{
        width: 155px;
        display: flex;
        align-items: center;
        justify-content: center;
        border: 1px solid #ADA4CD;
        cursor: pointer;
    }

    @media screen and (max-width: 700px) {
        #btn-login{
            display: none;
        }
    }
</style>
