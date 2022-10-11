<template>
  <div class="col-12 p-3" @click="showDropdown">
    <div class="d-flex">
        <font-awesome-icon 
            id="icons" 
            :class="[active ? 'active' : '', 'p-1 align-self-center']" 
            :icon="['fa-solid', active ? 'fa-minus' :'fa-plus']" />
        <h4 class="ps-3 text-uppercase m-0" >{{date.date}} {{date.place}}</h4>
    </div>
        
        <!-- DROPDOWN -->
        <div v-show="active" class="row p-4">
        <div id="googleMap" class="col-4 bg-light">mapppa</div>
            <div class="col-8 p-4">
                <h3>Untold stories</h3>
                <p>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Nostrum temporibus nulla animi soluta natus vero dolore aperiam blanditiis iusto expedita.</p>
                <button @click="stopPropagation($event)" class="ae-color">book now</button>
            </div>
        </div>
        <!-- end DROPDOWN -->
    </div>
</template>

<script>



export default {
    name: 'DropdownComponent',
    data(){return{
        active: false,
    }},
    props:{
        date: Object,
    },
    methods:{
        showDropdown(){           
            this.active = !this.active        
        },
        stopPropagation(event){
            event.stopPropagation()
        }
    }

}
</script>

<style scoped lang="scss">
@import '@/variables-utiles.scss';
.col-12{
    background-color: $median-charade;
    &:hover{
    background-color: $lynch;
    }&:hover #icons{
        background-color: $mandy;
    }
    cursor: pointer;
    h4{
        color: $mandy
    }
    #icons{
    color: $white;
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