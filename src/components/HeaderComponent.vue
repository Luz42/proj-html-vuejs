<template>
  <header>
    <div class="container-fluid">
      <section class="row p-3">
        <!-- LOGO -->
        <div class="col">
          <img src="@/assets/images/avada-music-logo.png" alt="">
        </div>
        <!-- MENU BARS -->
        <div class="col ae-flex-end-element">
          <font-awesome-icon icon="fa-solid fa-bars" style="font-size:2em" />
        </div>
      </section>
      <div class="row">
        <!-- CONTENT -->
        <section class="col ae-flex-center-element">
          <h1>Untold Stories</h1>
          <p>There is an untold story behind every favorite song.</p>
          <div class="text-uppercase d-flex gap-2 p-4">
            <button class="ae-color">latest album</button>
            <button>live dates</button>
          </div>
        </section>
        <!-- end CONTENT -->
      </div>
    </div>
  </header>
</template>

<script>
export default {
 name: 'HeaderComponent'
}
</script>

<style scoped lang="scss">
  @import '@/variables.scss';

  
  header{
    background-image: url('../assets/images/home_slider.jpg');
    background-position-y: center;
    background-size: cover;
    color: $white;
    .row .col.ae-flex-center-element{
      padding: 10%;
        h1{
        font-size: 7em;
        font-weight: bolder;
        };
        p{
          font-style: italic;
          font-family: $serif;
        }
        div{
        //   padding-bottom: 20% !important;
        // border-bottom: 20px solid $mandy !important;
          button{
            text-transform: uppercase;
            border: $white 1px solid;
            padding: 8px 25px;
            color: $white;
            background-color: rgba(255, 255, 255, 0);
            &.ae-color{
              background-color: $mandy;
              border: 0;
            }
          }
        }
        
    }
    
  }

</style>