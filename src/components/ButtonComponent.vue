<template>
  <button class="text-uppercase">views all {{ sectionName }}</button>
</template>

<script>
export default {
 name:'ButtonComponent',
 props:{
    sectionName: String
 }
}
</script>

<style scoped lang="scss">
@import '@/variables.scss';
    button{
        width: 100%;
        padding: 3%;
        color: $white;
        background-color: $mandy;
        border: 0;
        &:hover{
            color: black;
            background-color: $white;
        }
    }
</style>