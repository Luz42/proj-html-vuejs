<template>
  <main>
    <section id="Band-news">
    <SectionsTitlesComponent title="latest band news"/>
    <div class="container-xl pb-5">
      <div class="row">
        <div class="col-8">
          <div class="row">
            <div class="col-12 mb-4">
              <img class="img-fluid" src="@/assets/images/blog_music_techo-1200x600.jpg" alt="">
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
  </section>
  </main>
</template>

<script>
import SectionsTitlesComponent from './SectionsTitlesComponent.vue';
export default {
    name: "MainComponent",
    components: { 
      SectionsTitlesComponent
     }
}
</script>

<style scoped lang="scss">
  @import '@/variables.scss';

 main{
  background-color: $charade;
 }
</style>