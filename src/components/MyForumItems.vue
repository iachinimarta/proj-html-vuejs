<template>
  <div class="d_flex w_80 item_wrapper">
    <div class="item d_flex" v-for="(item, index) in shareData" :key="index">
        <a :href="item.link">
            <i class="item_icon fa-2x mb_10" :class="item.icon"></i>
            <p class="item_text">{{item.title}}</p>  
        </a>  
    </div>
  </div>
</template>

<script>
    export default {
        name: 'MyForumItems',
        props: {
            shareData: Array
        }
    }
</script>

<style lang="scss">
@import '@/styles/general.scss';

    .item_wrapper {
        flex-wrap: wrap;

        .item {
            width: calc(100% / 4 - 40px);
            height: 180px;
            border-top: 2px solid $brand-color-blue;
            margin: 10px 20px;
            justify-content: center;
            align-items: center;
            background-color: white;

            .item_icon {
                display: inline-block;
                background-color: #fc8c5e;
                border-radius: 50%;
                color: white;
                line-height: 65px;
                width: 70px;
            }

            .item_text {
                font-weight: bold;
            }
        }  
    }
    

</style>