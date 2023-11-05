<template>
    <div id="menu">
        <h6>Scarp.IT</h6>
        <div id="btn-wiki">
            <h6 style="font-family: 'Jet Brains'; margin: 0;"> Esteira </h6>
        </div>
    </div>
</template>

<script setup lang="ts">
    // function clickBtnWiki(){
    //     window.open('http://wiki.scarpit.tech', '_blank');
    // }
</script>


<style lang="scss" scoped>
    #menu{
        display: flex;
        width: 70vw;
        height: 60px;
        border-bottom: 1px solid #ADA4CD;
        justify-content: space-between;
        z-index: 10;
        font-size: 1.17em;
    }

    #btn-wiki{
        width: 155px;
        display: flex;
        align-items: center;
        justify-content: center;
        border: 1px solid #ADA4CD;
        // cursor: pointer;
    }

    h6{
        margin: 0;
        align-self: center;
    }
</style>
