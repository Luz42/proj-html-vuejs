<template>
  <div id="app">
    <HeaderComponent/>
    <MainComponent :dates="dates" :cards="cards"/>
    <FooterComponent/>
  </div>
</template>

<script>
import HeaderComponent from './components/HeaderComponent.vue';
import MainComponent from './components/MainComponent.vue';
import FooterComponent from './components/FooterComponent.vue';
import { cardsArray, liveDates } from './assets/images/data.js'


export default {
  name: 'App',
  data(){return{
    cards: [...cardsArray],
    dates: [...liveDates]
    }},
  components: {
    HeaderComponent,
    MainComponent,
    FooterComponent
  }
}
</script>

<style lang="scss">
  @import '~bootstrap/scss/bootstrap.scss';
  @import 'https://fonts.googleapis.com/css2?family=Lora&family=Source+Sans+Pro&display=swap';
  @import '@/variables-utiles.scss';

  .ae-flex-end-element{
    display: flex !important;
    justify-content: end !important;
    align-items: center !important;
  }

  .ae-flex-center-element{
    display: flex !important;
    justify-content: center !important;
    align-items: center !important;
    flex-direction: column;
  }

#app {
  font-family: $sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;

}
</style>
