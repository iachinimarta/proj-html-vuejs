<template>
  <main>

    <!-- JUMBOTRON -->

    <div class="jumbotron d_flex">
      <div class="jumbotron_text">
        <h1>Tech Forum!</h1>
        <p>Discuss all the latest technology news and trends</p>
        <button class="btn btn_2">
          <a href="#">GET AVADA NOW! ></a>
        </button>
      </div>
    </div>

    <!-- SEZIONE PLACE TO BE -->
    <div class="place_to_be t_center">
      <div class="place_to_be_text w_80">
        <h5>AVADA FORUM IS THE PLACE TO BE</h5>
        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Suscipit laboriosam debitis hic. Cumque facere sed veritatis ea inventore, et minima eum neque atque repellendus asperiores voluptatibus corrupti aut dolor quisquam sint, nihil deleniti delectus maiores magnam qui perferendis voluptate quaerat eos. Aspernatur ipsam rerum possimus eligendi tempore ducimus rem explicabo.</p>  
      </div>
    </div>

    <!-- SEZIONE ALL THE LATEST NEWS -->

    <div>
      <div class="t_center w_80">
        <h5>PHASELLUS EGET METUS</h5>
        <h2>All the latest news</h2>
      </div>
    </div>

    <hr>

    <!-- SEZIONE 3 IMGS -->

    <div>
      <div class="card">

        <!-- creare un array di img da stampare -->
        <img src="" alt="">
      </div>
    </div>

  </main>
</template>

<script>
    export default {
        name: 'MyMain'
    }
</script>

<style lang="scss">
@import '@/styles/general.scss';

  main {
    margin-top: 80px;
    
    .jumbotron {
      color: white;
      background-image: url('../assets/home_slider_bg.jpg');
      background-size: cover;
      background-position: center;
      min-height: 550px;
      justify-content: center;
      align-items: center;

      .jumbotron_text {
        h1 {
          font-size: 6rem;
        }
      }
    }

    .place_to_be {
      background-color: $brand-color-beige;
    }

    .card {
      width: calc(100% / 3);
    }
  }

  

</style>