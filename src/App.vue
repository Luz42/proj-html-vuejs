<template>
  <div id="app">
    <HeaderComponent/>
    <MainComponent :cards="cards"/>
    <FooterComponent/>
  </div>
</template>

<script>
import HeaderComponent from './components/HeaderComponent.vue';
import MainComponent from './components/MainComponent.vue';
import FooterComponent from './components/FooterComponent.vue';
import { cardsArray } from './assets/images/data.js'


export default {
  name: 'App',
  data(){return{
    cards: [...cardsArray]
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

  // @mixin button-layout{
  //   &:hover{
  //             background-color: $white !important;
  //             color: black;
  //           }
  //         text-transform: uppercase;
  //         border: $white 1px solid;
  //         padding: 8px 25px;
  //         color: $white;
  //         background-color: rgba(255, 255, 255, 0);
  //           &.ae-color{
  //             background-color: $mandy;
  //             border: 0;
  // }
  // };

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
