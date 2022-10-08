<template>
  <div class="col-12 p-3" @click="showDropdown">
    <div class="d-flex">
        <font-awesome-icon id="icons" :class="[active ? 'active' : '', 'p-1 align-self-center']" :icon="['fa-solid', active ? 'fa-minus' :'fa-plus']" />
            <!-- <font-awesome-icon v-else icon="fa-solid fa-minus" /> -->
        <h4 class="ps-3 text-uppercase m-0" >17/08/2020 gem festival 2020 anakalia, georgia</h4>
    </div>
        
        <!-- DROPDOWN -->
        <div v-show="active" class="row p-4">
        <div id="googleMap" class="col-4 bg-light">mapppa</div>
            <div class="col-8 p-4">
                <h3>Untold stories</h3>
                <p>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Nostrum temporibus nulla animi soluta natus vero dolore aperiam blanditiis iusto expedita.</p>
                <button class="ae-color">book now</button>
            </div>
        </div>
        <!-- end DROPDOWN -->
    </div>
</template>

<script>



export default {
    name: 'DropdownComponent',
    data(){return{
        active: false
    }},
    methods:{
        showDropdown(){
            this.active = !this.active
        }
    }

}
</script>

<style scoped lang="scss">
@import '@/variables-utiles.scss';
.col-12{
    background-color: $median-charade;
    cursor: pointer;
    h4,
    #icons{
        color: $mandy
    }
    #icons.active{
        background-color: $mandy;
        color: $white
    };
    h3{
        color: $white;
    }
    p{
        color: $bombay;
        font-family: $serif;
    };

    button{
        @include button-layout();
    }
}


</style>