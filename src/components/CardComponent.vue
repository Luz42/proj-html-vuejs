<template>
    <div :class="`ae-col-${card.col} p-3`">
        <div @mouseenter="unshowDescription" @mouseleave="showDescription" class="position-relative" style="height:100%">
            
            <img :src="require(`@/assets/images/blog${card.src}.jpg`)" alt="">
            
            <div v-if="descriptionVisible" class="start-0 bottom-0 w-100 position-absolute">
                <h3>{{ card.title }}</h3>
                <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit. Labore, quae numquam molestiae nobis magnam animi dolores.</p>
            </div>
            
            <div v-else class="position-absolute top-0 h-100 w-100 ae-flex-center-element">
                <h5>{{ card.title }}</h5>
            </div>
        
        </div>
    </div>
</template>

<script>
export default {
    name:'CardComponent',
    data(){return{
        descriptionVisible: true,
    }},
    props:{
        card: Object
    },
    methods:{
        unshowDescription(){
            this.descriptionVisible = false;
        },
        showDescription(){
            this.descriptionVisible = true
        },
    }
}

</script>

<style scoped lang="scss">
  @import '@/variables-utiles.scss';

img{
    object-fit: cover !important;
    height: 100% !important;
    width: 100% !important
};

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
    h5{
      color: $white;
      font-weight: bold;
    }
  }
</style>