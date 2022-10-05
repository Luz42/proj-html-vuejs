<template>
  <header>
    <div class="container-fluid">
      <div class="row p-3">
        <div class="col"><img src="@/assets/images/avada-music-logo.png" alt=""></div>
        <div class="col ae-flex-end-element">icona menu</div>
      </div>
      <div class="row">
        <div class="col p-5 ae-flex-center-element">
          <h1>Untold Stories</h1>
          <p>There is an untold story behind every favorite song.</p>
          <div class="text-uppercase">
            <button>latest album</button>
            <button>live dates</button>
          </div>
        </div>
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
    color: $white;
    h1{
      font-size: 8em;
      font-weight: bolder;
    };
    p{
      font-style: italic;
      font-family: $serif;
    }
    button{
      text-transform: uppercase;
    }
  }

</style>