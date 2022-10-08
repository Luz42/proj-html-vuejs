<template>
    <section class="container-fluid">
      <div class="row p-5 ae-flex-center-element">
        <div class="col-6 ae-flex-center-element text-center">
          <h2 class="m-0 text-capitalize">{{ title }}</h2>
          <hr class="w-25 m-4">
          <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Aliquam delectus culpa quas minima libero, esse omnis enim repellendus modi repudiandae maiores.</p>
        </div>
      </div>
    </section>
</template>

<script>
export default {
 name:'SectionTitlesComponent',
 props:{
    title: String
 }
}
</script>

<style scoped lang="scss">
  @import '@/variables.scss';

section.container-fluid{
      background-color: inherit;
      color: $white;


      }
      h2{
        font-size: 3em !important;
        font-weight: bold;

      };
      p{
        color: $bombay;
        font-family: $serif;
      }
    
</style>