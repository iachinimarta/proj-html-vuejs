<template>
  <footer class="fs_14">
    <div class="d_flex w_80 footer_container">
      <div class="d_flex">
        <div class="footer_description">
          <h4 class="mb_20">AVADA TECH FORUM</h4>
          <p>Sed sempre, nisl id feugiat eleifend, erat est digssim felis, quis auctor elit enim nec ante. Cras et nibh risus. Pellentesque non mi sit amet mi intermentum.</p>
        </div>
        <MyLink :array="popular"/>
        <MyLink :array="recent"/>
        <MyLink :array="latest"/>
      </div>
    </div>

    <div class="copyright">
      <div class="w_80 d_flex footer_bottom">
        <p>
          &copy; Copyright 2012 - 2020 | Avada Theme by <a href="#"><b>Theme Fusion</b></a> | All Rights Reserved | Powered by <a href="#"><b>WordPress</b></a>
        </p>
        <div class="icon_container d_flex">
          <a href="#"><i class="fa-brands fa-facebook-f"></i></a>
          <a href="#"><i class="fa-brands fa-twitter"></i></a>
          <a href="#"><i class="fa-brands fa-instagram"></i></a>
          <a href="#"><i class="fa-brands fa-youtube"></i></a>  
        </div>
      </div>
      
    </div>
    
  </footer>
</template>

<script>
import MyLink from './MyLink.vue';

    export default {
        name: 'MyFooter',
        components: {
          MyLink
        }, 
        data() {
          return {               
            popular: 
              [{
                title: 'POPULAR TOPICS',
                link: '#',
                icon: 'fa-solid fa-angle-right',
                text: {
                  a: 'Nam a dolor volutpat massa auctor semper',
                  b: 'Sed euismod nunc urna fermentum arcu dapibus fringilla',
                  c: 'Cras lacinia tellsus id mauris finibus lacus molestie',
                  d: 'Curabitur a scelerisque ligula'
                }               
              }],
            recent: [{
              title: 'RECENT TOPICS',
              link: '#',
              icon: 'fa-solid fa-angle-right',
              text: {
                  a: 'Cras lacinia tellsus id mauris finibus lacus molestie',
                  b: 'Proin at ligula sagittis vestibulum nisi vitae',
                  c: 'Sed nec metus at est tincidunt elementum',
                  d: 'Nulla egestas nulla eu nulla suscipit molestie'
              }     
            }],
            latest: [{
              title: 'LATEST REPLIES',
              link: '#',
              icon: 'fa-solid fa-angle-right',
              text: {
                  a: 'Cras lacinia tellsus id mauris finibus lacus molestie',
                  b: 'Cras lacinia tellsus id mauris finibus lacus molestie',
                  c: 'Nulla egestas nulla eu nulla suscipit molestie',
                  d: 'Mauris ac nibh quis eros sagittis lacinia a et dui'
              }  
            }]
          }        
        }
      }
</script>

<style lang="scss">
@import '@/styles/general.scss';

  footer {
    height: 400px;

    .footer_container {
      align-items: center;
      height: 100%;
      
      .footer_description {
        width: 35%;
      }
    }

    .copyright {
      border-top: 1px solid lightgray;

      .footer_bottom {
        justify-content: space-between;
        align-items: center;
        height: 100px;

        .icon_container {
          justify-content: center;
          align-items: center;

          a {
            margin: 0 5px;
          }

          .fa-brands {
            border-radius: 50%;
            color: white;
            line-height: 30px;
            width: 30px;
            text-align: center;
          }

          .fa-facebook-f {
            background-color: #4562b0;              
          }

          .fa-twitter {
            background-color: #74def4;
          }

          .fa-instagram {
            background-color: #399bc0;
          }

          .fa-youtube {
            background-color: #bf2717;
          }
        }
      }
    }
  }

</style>