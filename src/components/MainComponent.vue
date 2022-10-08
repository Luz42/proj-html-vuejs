<template>
  <main>
    <section id="Band-news">
    <SectionsTitlesComponent title="latest band news"/>
    <div class="container-xl pb-5">
      <div class="row">
        <div class="col-8">
          <div class="row">
            <div class="col-12 mb-4">
              <div class="position-relative">
                <img class="img-fluid" src="@/assets/images/blog_music_techo-1200x600.jpg" alt="">
                <div class="start-0 bottom-0 w-100 position-absolute">
                  <h3>tecnology and music</h3>
                  <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit. Labore, quae numquam molestiae nobis magnam animi dolores.</p>
                </div>
                <div class="position-absolute top-0 h-100 w-100 ae-flex-center-element">
                  <h3>tecnology and music</h3>
                </div>
              </div>
            </div>
            <div class="col-6">
              <img class="img-fluid" src="@/assets/images/blog-post3-600x900.jpg" alt="">
            </div>
            <div class="col-6">
              <img class="img-fluid" src="@/assets/images/blog-post4-600x900.jpg" alt="">
            </div>
            <div class="col-12 mt-4">
              <img class="img-fluid" src="@/assets/images/blog_flavor_rock-1200x600.jpg" alt="">
            </div>
          </div>
        </div>
        <div class="col-4 d-flex">
          <div class="row gap-4">
            <div class="col-12">
              <img style="height:100%; object-fit: cover;" class="img-fluid" src="@/assets/images/blog-post1-600x900.jpg" alt="">
            </div>
            <div class="col-12">
              <img style="height:100%; object-fit: cover;" class="img-fluid" src="@/assets/images/blog-post2-600x900.jpg" alt="">
            </div>
          </div>
        </div>
      </div>
    </div>
    <ButtonComponent sectionName="latest news"/>
  </section>
  <section id="Live-dates">
    <div class="text-center">
      <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Rerum nisi suscipit, mollitia fugiat officiis molestiae totam, sit reprehenderit laborum, unde tempora explicabo at neque non doloremque magni assumenda quas tenetur!</p>
      <img src="@/assets/images/band_interview_play_icon.png" alt="">
    </div>
    <SectionsTitlesComponent title="live dates"/>
    <div class="container-xl">
      <div class="row gap-3">
        <DropdownComponent/>
      </div>
    </div>
  </section>
  </main>
</template>

<script>
import SectionsTitlesComponent from './SectionsTitlesComponent.vue';
import ButtonComponent from './ButtonComponent.vue';
import DropdownComponent from './DropdownComponent.vue';

export default {
    name: "MainComponent",
    components: {
    SectionsTitlesComponent,
    ButtonComponent,
    DropdownComponent
},
     
  }
</script>

<style scoped lang="scss">
  @import '@/variables-utiles.scss';

 main{
  background-color: $charade;
  .position-absolute.bottom-0{
    background-color: $median-charade;
    padding: 2% 5%;
    h3{
    color: $mandy;
    }
    p{
      color: $bombay;
    }
  }
  .position-absolute.h-100{
    background-color: $design-mandy;
    h3{
      color: $white;
      font-weight: bold;
    }
  }
  #Live-dates .text-center{
    background-image: url('@/assets/images/home-testimonial-parallax.jpg');
    background-position-y: center;
    background-size: cover;
    color: $white;
    padding: 10% 20%;
    p{
      font-style: italic;
      font-family: $serif;
      //font-size: 1.2em
    }
  }  
 }
</style>