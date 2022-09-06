<template>
  <main>

    <!-- JUMBOTRON -->

    <div class="jumbotron d_flex">
      <div class="jumbotron_text">
        <h1>Tech Forum!</h1>
        <p>Discuss all the latest technology news and trends</p>
        <button class="btn btn_2">
          <a href="#">GET AVADA NOW! <i class="fa-solid fa-angle-right"></i></a>
        </button>
      </div>
    </div>

    <!-- SEZIONE PLACE TO BE -->
    <div class="bg_beige t_center">
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
  
      <div class="w_80 ">

        <!-- 3 IMGS -->
        <MyNewsItems :shareData="newsData_1"/>

        <!-- SEZIONE FEATURED ARTICLES -->
        <div class="article featured_article">
          <h5>FEATURED ARTICLE</h5>
          <h1>Cras malesuada et orci eget pharetra</h1>
          <p>In quis lectus sed leo elementum faucibus in dapibus dictum. Nullamolestie tortor nec lectus venenatis, sed blandit dui, dolor at bibendum sadipis ets ipsums dolores ficilis uns leo lectus.</p>
          <button class="btn btn_1">
            <a href="#">READ MORE <i class="fa-solid fa-angle-right"></i></a>
          </button>
        </div>

        <!-- 3 IMGS -->
        <MyNewsItems :shareData="newsData_2"/>

        <!-- SEZIONE REVIEWED PRODUCT -->
        <div class="article reviewd_product">
          <h5>FEATURED ARTICLE</h5>
          <h1>Cras malesuada et orci eget pharetra</h1>
          <p>In quis lectus sed leo elementum faucibus in dapibus dictum. Nullamolestie tortor nec lectus venenatis, sed blandit dui, dolor at bibendum sadipis ets ipsums dolores ficilis uns leo lectus.</p>
          <button class="btn btn_1">
            <a href="#">READ MORE <i class="fa-solid fa-angle-right"></i></a>
          </button>
        </div>
      </div>

  </main>
</template>

<script>
import MyNewsItems from '../components/MyNewsItems.vue';

  export default {
      name: 'MyMain',
      components: {
        MyNewsItems,
      },
      data() {
        return {
          newsData_1: [
                  {
                    src: require('../assets/post_feat_img_25-700x441.jpg'),
                    alt: 'smartphone',
                    title: 'Morbi vitae dui euismod vulputate sollicitudin',
                    date: 'October 11th, 2015',
                    comments: '2 Comments',
                    active: true,
                    p: 'Donec finibus sit amet orci eget ultricies. Praesent posuere ante ut erat fringilla, vestibulum placerat metus mattis. Aenean dictum vitae nisl'
                  },
                  {
                    src: require('../assets/post_feat_img_24-700x441.jpg'),
                    alt: 'smartphone',
                    title: 'Vivamus pellenteque, felis quis varius',
                    date: 'October 11th, 2015',
                    comments: '2 Comments',
                    active: false,
                    p: 'Donec finibus sit amet orci eget ultricies. Praesent posuere ante ut erat fringilla, vestibulum placerat metus mattis. Aenean dictum vitae nisl'
                  },
                  {
                    src: require('../assets/post_feat_img_23-700x441.jpg'),
                    alt: 'smartwatch',
                    title: 'Donec ornare pretium eget scelisque justo',
                    date: 'October 11th, 2015',
                    comments: '2 Comments',
                    active: false,
                    p: 'Donec finibus sit amet orci eget ultricies. Praesent posuere ante ut erat fringilla, vestibulum placerat metus mattis. Aenean dictum vitae nisl'
                  },
          ],
          newsData_2: [
            {
              src: require('../assets/post_feat_img_22-700x441.jpg'),
              alt: 'tablet',
              title: 'Fusce sollicitudin nunc sed placerat varius',
              date: 'October 11th, 2015',
              comments: '2 Comments',
              active: false,
              p: 'Donec finibus sit amet orci eget ultricies. Praesent posuere ante ut erat fringilla, vestibulum placerat metus mattis. Aenean dictum vitae nisl'
            },
            {
              src: require('../assets/post_feat_img_21-700x441.jpg'),
              alt: 'camera',
              title: 'Donec facilis sodales leo sit amet laoreet',
              date: 'October 11th, 2015',
              comments: '2 Comments',
              active: false,
              p: 'Donec finibus sit amet orci eget ultricies. Praesent posuere ante ut erat fringilla, vestibulum placerat metus mattis. Aenean dictum vitae nisl'
            },
            {
              src: require('../assets/post_feat_img_20-700x441.jpg'),
              alt: 'laptop',
              title: 'Proin eu purus sed aru aliquet curabir vens',
              date: 'October 11th, 2015',
              comments: '2 Comments',
              active: false,
              p: 'Donec finibus sit amet orci eget ultricies. Praesent posuere ante ut erat fringilla, vestibulum placerat metus mattis. Aenean dictum vitae nisl'
            },
          ],
        }
      }
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

    .article {
      min-height: 400px;
      background-size: cover;
      background-position: center;
      color: white;
    }

    .featured_article {
      background-image: url('../assets/featured_article_1_bg.jpg');
    }

    .reviewd_product {
      background-image: url('../assets/featured_article_2_bg.jpg');
    }
    
  }

  

</style>