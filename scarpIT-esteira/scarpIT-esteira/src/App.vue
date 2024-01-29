<template>
  <main>
    <Menu></Menu>
    <div id="form-sonar">
      <div class="row">
        <div class="col-6 q-pa-sm">
          <q-input filled v-model="text" label="Nome da sua Esteira" color="grey-6" label-color="grey-6" :dense="true" :dark="true" />
        </div>
        <div class="col-6 q-pa-sm">
          <q-input filled v-model="text" label="Github URL" color="grey-6" label-color="grey-6" :dense="true" :dark="true"/>
        </div>
        <div class="col-6 q-pa-sm">
          <q-btn-toggle
            v-model="model"
            spread
            no-caps
            toggle-color="grey-10"
            color="grey-5"
            text-color="black"
            :options="[
            {label: 'Stress', value: 'stress'},
            {label: 'Load', value: 'load'}
        ]"
      />
        </div>
        <div class="col-6 q-pa-sm">
          <q-input filled v-model="text" label="Path Token" color="grey-6" label-color="grey-6" :dense="true" :dark="true"/>
        </div>
        <div class="col-4 q-pa-sm">
          <q-input filled v-model="text" label="VU Count" color="grey-6" label-color="grey-6" :dense="true" :dark="true"/>
        </div>
        <div class="col-4 q-pa-sm">
          <q-input filled v-model="text" label="Test Duration" color="grey-6" label-color="grey-6" :dense="true" :dark="true"/>
        </div>
        <div class="col-4 q-pa-sm">
          <q-item tag="label" v-ripple>
            <q-item-section>
              <q-item-label>Sonar Cub</q-item-label>
            </q-item-section>
            <q-item-section avatar>
              <q-toggle color="blue" v-model="notifications" val="battery" />
            </q-item-section>
          </q-item>
        </div>
      </div>
    </div>
    <div id="button" class="q-pt-lg">
      <button>RUN</button>
    </div>
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
        display: grid;
    }

    #form-sonar{
      // height: 30vh;
      display: flex;
      flex-direction: column;
      width: 70vw;
      margin-top: 20vh;
      padding: 20px;
      border-radius: 5px;
      background: rgba(0,0,0,.07);
      box-shadow: 4px 4px 4px #00000040;
      backdrop-filter: blur(5px);
      -webkit-backdrop-filter: blur(5px);
      z-index: 10;

      > div{
        width: 100%;
        // height: min(100%, 30px);
      }
    }

    button{
      width: 100%;
      font-size: 1rem;
    }

    button:hover{
        border-color: rgba(255, 255, 255, 0.308);
        box-shadow: rgba(0, 0, 0, 0.25) 0px 54px 55px, rgba(0, 0, 0, 0.12) 0px -12px 30px, rgba(0, 0, 0, 0.12) 0px 4px 6px, rgba(0, 0, 0, 0.17) 0px 12px 13px, rgba(0, 0, 0, 0.09) 0px -3px 5px;
    }
</style>
