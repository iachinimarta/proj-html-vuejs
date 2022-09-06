<template>
  <footer class="d_flex w_80">
    <div class="footer_items">
      <h5 class="mb_20">AVADA TECH FORUM</h5>
      <p>Sed sempre, nisl id feugiat eleifend, erat est digssim felis, quis auctor elit enim nec ante. Cras et nibh risus. Pellentesque non mi sit amet mi intermentum.</p>
    </div>
    <MyFooterLinks :shareData="topics"/>
  </footer>
</template>

<script>
import MyFooterLinks from '../components/MyFooterLinks.vue';

    export default {
        name: 'MyFooter',
        components: {
          MyFooterLinks
        }, 
        data() {
          return {
            topics: [{                
              popular: 
              {
                title: 'POPULAR TOPICS',
                link: '#',
                text: 'Nam a dolor volutpat massa auctor semper',
                icon: 'fa-solid fa-angle-right'
              },
              recent: {
                title: 'RECENT TOPICS',
                link: '#',
                text: 'Sed euismod nunc urna fermentum arcu dapibus fringilla',
                icon: 'fa-solid fa-angle-right'
              },
              latest: {
                title: 'LATEST REPLIES',
                link: '#',
                text: 'Cras lacinia tellsus id mauris finibus lacus molestie',
                icon: 'fa-solid fa-angle-right'
              },
            }]          
          }
        }
    }
</script>

<style lang="scss">
@import '@/styles/general.scss';

  footer {
    height: 400px;

    .footer_items {
      width: calc(100% / 4);
    }
  }

</style>