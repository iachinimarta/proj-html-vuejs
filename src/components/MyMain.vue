<template>
  <main>

    <!-- JUMBOTRON -->
    <div class="jumbotron d_flex">
      <div class="jumbotron_text">
        <h1>Tech Forum!</h1>
        <p class="mb_20 fs_14">Discuss all the latest technology news and trends</p>
        <button class="btn btn_2">
          <a href="#">GET AVADA NOW! <i class="fa-solid fa-angle-right"></i></a>
        </button>
      </div>
    </div>

    <!-- SEZIONE PLACE TO BE -->
    <div class="bg_beige beige_section d_flex">
      <div class="place_to_be_text w_80 t_center">
        <h5 class="mb_20">AVADA FORUM IS THE PLACE TO BE</h5>
        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Suscipit laboriosam debitis hic. Cumque facere sed veritatis ea inventore, et minima eum neque atque repellendus asperiores voluptatibus corrupti aut dolor quisquam sint, nihil deleniti delectus maiores magnam qui perferendis voluptate quaerat eos. Aspernatur ipsam rerum possimus eligendi tempore ducimus rem explicabo.</p>  
      </div>
    </div>

    <!-- SEZIONE ALL THE LATEST NEWS -->
    <div class="t_center mt_20">
      <h5 class="mb_20">PHASELLUS EGET METUS</h5>
      <h2 class="mb_20">All the latest news</h2>
      
      <hr class="mb_20">
    </div>

    <div class="w_80 mt_20">

      <!-- 3 IMGS -->
      <MyNewsItems :shareData="newsData_1"/>

      <!-- SEZIONE FEATURED ARTICLES -->
      <div class="article featured_article d_flex">
        <div class="featured_container">
          <h5 class="mb_20">FEATURED ARTICLE</h5>
          <h1 class="mb_20">Cras malesuada et orci eget pharetra</h1>
          <p class="mb_20 fs_14">In quis lectus sed leo elementum faucibus in dapibus dictum. Nullamolestie tortor nec lectus venenatis, sed blandit dui, dolor at bibendum sadipis ets ipsums dolores ficilis uns leo lectus.</p>
          <button class="btn btn_1">
            <a href="#">READ MORE <i class="fa-solid fa-angle-right"></i></a>
          </button>
        </div>
        
      </div>

      <!-- 3 IMGS -->
      <MyNewsItems :shareData="newsData_2"/>

      <!-- SEZIONE REVIEWED PRODUCT -->
      <div class="sided_section d_flex">
        <div class="article reviewd_product d_flex">
          <div>
            <h5 class="mb_20">REVIEWED PRODUCT</h5>
            <h1 class="mb_20">Cras malesuada et orci eget pharetra</h1>
            <p class="mb_20 fs_14">In quis lectus sed leo elementum faucibus in dapibus dictum. Nullamolestie tortor nec lectus venenatis, sed blandit dui, dolor at bibendum sadipis ets ipsums dolores ficilis uns leo lectus.</p>
            <button class="btn btn_1">
              <a href="#">READ MORE <i class="fa-solid fa-angle-right"></i></a>
            </button>
          </div>      
        </div>
        
        <!-- SEZIONE TUTORIALS & GUIDES -->
        <div class="tutorials">
          <h4 class="mb_20">Tutorials &amp; Guides</h4>
          <hr>

          <MyTutorialLinks :shareData="tutorialsLinks"/>

        </div>
      </div>
    </div>

    <!-- SEZIONE READ OUR BLOG -->
    <div class="black_section d_flex">
      <a href="#">READ OUR BLOG <i class="fa-solid fa-right-long ml_10"></i></a>
    </div>

    <!-- SEZIONE FORUM SECTIONS -->
    <div class="forum_sections bg_beige">
      <div class="t_center">
        <h5 class="mb_20">PHASELLUS EGET METUS</h5>
        <h2 class="mb_20">Forum Sections</h2>
        
        <hr class="mb_20">

        <MyForumItems :shareData="forumSections"/>
      </div>
    </div>

    <!-- SEZIONE OUR FORUM -->
    <div class="black_section d_flex">
      <a href="#">GO TO OUR FORUM <i class="fa-solid fa-right-long ml_10"></i></a>
    </div>

    <!-- SEZIONE JOIN OUR COMMUNITY -->
    <div class="our_community article d_flex">
      <div class="our_community_text t_center">
        <h1 class="mb_20">Hey! Join to our Community</h1>
        <p class="mb_20 fs_14">Nulla molestie tortor nec lectus venenatis, sed blandit dui finibus. Curabitur feugiat vuluptate purus ipsums dolores ficilis uns etra.</p>
        <button class="btn btn_2">
          <a href="#">SIGN UP <i class="fa-solid fa-angle-right"></i></a>
        </button>
      </div>    
    </div>

    <!-- SEZIONE SUBSCRIBE -->
    <div class="bg_beige beige_section d_flex">
      <div class="t_center w_80">
        <h3 class="mb_20">Subscribe to our Newsletter</h3>
        <input type="email" placeholder="Insert your email*" class="subscribe_input" required>
        <button class="btn btn_1">
          <a href="#">SEND</a>
        </button>
      </div>
    </div>
  </main>
</template>

<script>
import MyNewsItems from '../components/MyNewsItems.vue';
import MyForumItems from '../components/MyForumItems.vue';
import MyTutorialLinks from '../components/MyTutorialLinks.vue';

  export default {
      name: 'MyMain',
      components: {
        MyNewsItems,
        MyForumItems,
        MyTutorialLinks
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
          forumSections: [
            {
              title: 'News & Community',
              link: '#',
              icon: 'fa-solid fa-file-lines'
            },
            {
              title: 'Apple Forum',
              link: '#',
              icon: 'fa-brands fa-apple'
            },
            {
              title: 'Microsoft Forum',
              link: '#',
              icon: 'fa-brands fa-windows'
            },
            {
              title: 'Android Forum',
              link: '#',
              icon: 'fa-brands fa-android'
            },
            {
              title: 'General Discussion',
              link: '#',
              icon: 'fa-solid fa-mug-saucer'
            },
            {
              title: 'Apps & Software',
              link: '#',
              icon: 'fa-solid fa-cubes'
            },
            {
              title: 'Gadgets & Stuff',
              link: '#',
              icon: 'fa-solid fa-laptop'
            },
            {
              title: 'Tutorials & Guides',
              link: '#',
              icon: 'fa-solid fa-wrench'
            }
          ],
          tutorialsLinks: [
            {
              src: require('../assets/post_feat_img_23-177x142.jpg'),
              title: 'Donec ornare pretium eget scelisque justo',
              link: '#',
              date: 'October 11th, 2015',
              active: false,
              alt: 'smartwatch'
            },
            {
              src: require('../assets/post_feat_img_22-177x142.jpg'),
              title: 'Fusce sollicitudin nunc sed placerat varius',
              link: '#',
              date: 'October 11th, 2015',
              active: false,
              alt: 'tablet'
            },
            {
              src: require('../assets/post_feat_img_20-177x142.jpg'),
              title: 'Proin eu purus sed aru aliquet curabir vens',
              link: '#',
              date: 'October 11th, 2015',
              active: false,
              alt: 'laptop'
            }
          ]
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

    .featured_article {
      background-image: url('../assets/featured_article_1_bg.jpg');
      margin: 50px 0;
    }

    .reviewd_product {
      background-image: url('../assets/featured_article_2_bg.jpg');
      width: 70%;
      margin: 40px 0 80px 0;
    }

    .tutorials {
      margin: 40px 0 80px 30px;
    }

    .forum_sections {
      height: 600px;
      padding-top: 40px;
    }

    .our_community {
      background-image: url('../assets/join_now_cta_bg.jpg');
      justify-content: center;
      align-items: center;

      .our_community_text {
        width: 30%;
      }
    }

    .subscribe_input {
        display: inline-block;
        border: 1px solid lightgray;
        width: 300px;
        height: 30px;
        margin-right: 25px;
    }
    
  }
</style>