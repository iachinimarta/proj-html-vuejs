<template>
  <header>

    <div class="bg_brandColor">
      <div class="header_container w_80 d_flex">
        <div class="header_logo">
          <a href="#">
            <img src="../assets/logo-2x.png" alt="logo">
          </a>
        </div>

        <div class="header_links d_flex">
          <ul class="d_flex">
            <li v-for="(links, index) in headerLinks" :key="index" @click="indexOfCurrentPage(index)" :class="(index == currentPage)?'active':''">
              <a :href="links.link">{{links.name}}</a>
            </li>
          </ul>

          <button class="btn btn_1">
            <a href="#">JOIN US</a>
          </button>

          <i class="fa-solid fa-magnifying-glass"></i>
        </div>
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
            ],
            currentPage: 0,
          }
        },
        methods: {
          indexOfCurrentPage(index) {
            this.currentPage = index;
            console.log(index);
          },
        }
    }
</script>

<style lang="scss">
@import '@/styles/general.scss';

  header {
    width: 100%;
    height: 90px;
    position: fixed;
    top: 0;
    left: 0;
    z-index: 999;

    .header_container {
      color: white;
      justify-content: space-between;
      align-items: center;
      padding: 15px;

      .header_links {
        align-items: center;

        .active {
          border-bottom: 2px dotted white;
          padding-bottom: 1px;
        }

        ul {
          margin-right: 10px;
        }

        .fa-magnifying-glass {
          margin-left: 20px;
        }
      }

      .header_logo {
        img {
          width: 200px;
        }
      }
    }
  }
</style>