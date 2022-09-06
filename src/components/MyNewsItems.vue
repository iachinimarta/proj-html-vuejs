<template>
  <div class="news_wrapper d_flex" >
    <div class="news" v-for="(news, index) in shareData" :key="index">
        <img class="news_img" :src="news.src" :alt="news.alt">
        <h4>{{news.title}}</h4>
        <p>{{news.date}} | </p>
        <p v-if="news.active">{{news.comments}}</p>
        <p v-else>Comments Off</p>
        <p>{{news.p}}</p>
    </div>
  </div>
</template>

<script>
    export default {
        name: 'MyNewsItems',
        data() {
            return {}                
        },
        props: {
            shareData: Array
        }
    }
</script>

<style lang="scss">
@import '@/styles/general.scss';

.news_wrapper {
    width: 100%;
    height: 100%;
    flex-wrap: wrap;

    .news {
        width: calc(100% / 3);

        img {
            width: 100%;
        }
    }
}
</style>