<template>
  <main>
    <Menu></Menu>
    <div id="form-sonar">
      <div class="row">
        <div class="col-6">
          <q-input filled v-model="text" :dense="true" />
        </div>
        <div class="col-6"></div>
      </div>
      <div class="row"></div>
      <div class="row"></div>
    </div>
    <div id="form-postman"></div>
    <div id="form-k6"></div>
  </main>
</template>

<script setup lang="ts">
  import { ref } from 'vue';
  import Menu from './components/Menu.vue';

  const text = ref();
</script>

<style scoped lang="scss">
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
        overflow: hidden;
    }

    #form-sonar{
      height: 30vh;
      display: flex;
      flex-direction: column;
      

      > div{
        width: 100%;
        height: min(100%, 30px);
      }
    }
</style>
