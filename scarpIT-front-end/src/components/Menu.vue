<template>
    <div id="menu">
        <h3 style="font-family: 'Jet Brains';">Scarp.IT</h3>
        <div id="btn-wiki" :onclick="clickBtnWiki">
            <h2 style="font-family: 'Jet Brains'; margin: 0;">Wiki</h2>
        </div>
    </div>
</template>

<script setup lang="ts">
    function clickBtnWiki(){
        window.open('https://www.scarpit.tech/wiki', '_blank');
    }
</script>


<style scoped lang="scss">
    #menu{
        display: flex;
        width: 70vw;
        height: 60px;
        border-bottom: 1px solid #ADA4CD;
        justify-content: space-between;
    }

    #btn-wiki{
        width: 155px;
        display: flex;
        align-items: center;
        justify-content: center;
        border: 1px solid #ADA4CD;
        cursor: pointer;
    }
</style>
