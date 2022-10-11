<template>
  <main>
    <!-- LATEST BAND NEWS -->
  <section id="Band-news">
    <SectionsTitlesComponent title="latest band news"/>
    <div class="container-xl pb-5">
      <CardContainer :cards="cards" />  
    </div>
    <ButtonComponent sectionName="latest news"/>
  </section>
    <!-- end LATEST BAND NEWS -->

  <section id="Live-dates">
    <div class="text-center">
      <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Rerum nisi suscipit, mollitia fugiat officiis molestiae totam, sit reprehenderit laborum, unde tempora explicabo at neque non doloremque magni assumenda quas tenetur!</p>
      <img src="@/assets/images/band_interview_play_icon.png" alt="">
    </div>
    <SectionsTitlesComponent title="live dates"/>
    <div class="container-xl pb-5">
      <div class="row gap-3">
        <DropdownComponent :date="date" :index="index" v-for="(date, index) in dates" :key="date.date"/>
      </div>
    </div>
    <ButtonComponent sectionName="live dates"/>
  </section>
  </main>
</template>

<script>
import SectionsTitlesComponent from './SectionsTitlesComponent.vue';
import ButtonComponent from './ButtonComponent.vue';
import DropdownComponent from './DropdownComponent.vue';
import CardContainer from './CardContainer.vue';


export default {
    name: "MainComponent",

    props:{
      cards: Array,
      dates: Array
    },
    components: {
    SectionsTitlesComponent,
    ButtonComponent,
    DropdownComponent,
    CardContainer
    }
  }
</script>

<style scoped lang="scss">
  @import '@/variables-utiles.scss';

 main{
  background-color: $charade;

  #Live-dates .text-center{
    background-image: url('@/assets/images/home-testimonial-parallax.jpg');
    background-position-y: center;
    background-size: cover;
    color: $white;
    padding: 10% 20%;
    p{
      font-style: italic;
      font-family: $serif;
    }
  }  
 }
</style>