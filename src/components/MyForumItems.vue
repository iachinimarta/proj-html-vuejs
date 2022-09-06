<template>
  <div class="d_flex w_80 item_wrapper">
    <div class="item d_flex" v-for="(item, index) in shareData" :key="index">
        <a :href="item.link">
            <i class="item_icon fa-2x" :class="item.icon"></i>
            <p>{{item.title}}</p>  
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
            border: 1px solid black;
            margin: 10px 20px;
            justify-content: center;
            align-items: center;

            .item_icon {
                display: inline-block;
                background-color: $brand-color-orange;
                border-radius: 50%;
                padding: 23px 25px;
            }
        }  
    }
    

</style>