<template>
  <div id="gridContainer">
      <CardComponent :card="card" v-for="card in cards" :key="card.col"/>
  </div>
</template>

<script>
import CardComponent from './CardComponent.vue'

export default {
    name:'CardContainer',
    props:{
      cards: Array
    },
    components:{
        CardComponent
    }
}
</script>

<style scoped lang="scss">
#gridContainer{
    display: grid;
    grid-template-columns: calc(100% / 3);
    grid-template-rows: calc(100% / 4);
    .ae-col-1{
        grid-column-start: 1;
        grid-column-end: 3;
        grid-row-start: 1;
        grid-row-end: 2;
    };
    .ae-col-2{
        grid-column-start: 3;
        grid-column-end: 4;
        grid-row-start: 1;
        grid-row-end: 3;
    }
    .ae-col-3{
        grid-column-start: 1;
        grid-column-end: 2;
        grid-row-start: 2;
        grid-row-end: 4;

    }
    .ae-col-4{
        grid-column-start: 2;
        grid-column-end: 3;
        grid-row-start: 2;
        grid-row-end: 4;

    }
    .ae-col-5{
        grid-column-start: 3;
        grid-column-end: 4;
        grid-row-start: 3;
        grid-row-end: 5;
    }
    .ae-col-6{
        grid-column-start: 1;
        grid-column-end: 3;
        grid-row-start: 4;
        grid-row-end: 5;
    }
}
</style>