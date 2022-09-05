<template>
  <header>
    <!-- HEADER -->
    <div class="container-fluid bg_brandColor">
      <div class="row ">
        <div class="col"></div>
        <div class="col-8">
          <div class="row">
            <div class="col-3">
              <img class="img-fluid" src="../assets/logo-2x.png" alt="logo">
            </div>
            <ul class="col-9 d-flex justify-content-end">
              <li v-for="(link, index) in headerLinks" :key="index"> <a :href="link.link">{{link.name}}</a> </li>
            </ul>
          </div>
        </div>
        <div class="col"></div>
      </div>
    </div>

    <!-- JUMBOTRON -->
    <div class="container-fluid jumbotron">
      <div class="row ">
        <div class="col"></div>
        <div class="col-8">AREA TESTO</div>
        <div class="col"></div>
      </div>
    </div>
  </header>
</template>

<script>
    export default {
        name: 'MyHeader',
        data() {
          return {
            headerLinks: [
              {
                name: 'Home',
                link: '#'
              },
              {
                name: 'Apple',
                link: '#'
              },
              {
                name: 'Microsoft',
                link: '#'
              },
              {
                name: 'Android',
                link: '#'
              },
              {
                name: 'Forums',
                link: '#'
              },
              {
                name: 'Contact us',
                link: '#'
              },
            ]
          }
        }
    }
</script>

<style lang="scss">
  @import '@/styles/general.scss';

  .jumbotron {
    height: 300px;
    width: 100%;
    background-image: url('../assets/home_slider_bg.jpg');
    background-position: center;
  }

</style>