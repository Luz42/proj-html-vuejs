<template>
  <main>
    <SectionsTitlesComponent title="latest band news"/>
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