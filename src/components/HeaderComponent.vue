<template>
  <header>
    <div class="container-fluid">
      <section class="row p-3">
        <!-- LOGO -->
        <div class="col">
          <img src="@/assets/images/avada-music-logo.png" alt="">
        </div>
        <!-- MENU BARS -->
        <div class="col ae-flex-end-element">
          <font-awesome-icon icon="fa-solid fa-bars" style="font-size:2em" />
        </div>
      </section>
      <div class="row">
        <!-- CONTENT -->
        <section class="col ae-flex-center-element">
          <h1>Untold Stories</h1>
          <p>There is an untold story behind every favorite song.</p>
          <div class="text-uppercase d-flex gap-2 p-4">
            <button class="ae-color">latest album</button>
            <button>live dates</button>
          </div>
        </section>
        <!-- end CONTENT -->
      </div>
    </div>
    <!-- SECTION WITH COLORED BAR -->
    <div class="position-relative">
      <div id="ae-bar"></div>
      <SectionsTitlesComponent title="music is life"/>
    </div>
    <!-- end SECTION WITH COLORED BAR -->
</header>
</template>

<script>
import SectionsTitlesComponent from './SectionsTitlesComponent.vue';

export default {
 name: 'HeaderComponent',
 components:{
    SectionsTitlesComponent,
}
}
</script>

<style scoped lang="scss">
  @import '@/variables-utiles.scss';


  
  header{
    background-image: url('../assets/images/home_slider.jpg');
    background-position-y: center;
    background-size: cover;
    color: $white;
    section.col.ae-flex-center-element{
      padding: 10%;
        h1{
        font-size: 7em;
        font-weight: bolder;
        };
        p{
          font-style: italic;
          font-family: $serif;
          font-size: 1.2em
        }

        button{
            @include button-layout()
        } 
    }
  }
  .position-relative{
    background-color: $median-charade;
      #ae-bar{
      position: absolute;
      padding: 6px 150px;
      background-color: $mandy;
      left: 50%;
      transform: translateX(-50%);
   }
  }
   
</style>