<template>
    <div>
        <div v-for="(item, index) in shareData" :key="index" class="d_flex links_container">
            <div>
                <h4 class="mb_20">{{item.popular.title}}</h4>
                <div class="d_flex mb_20">
                        <i :class="item.popular.icon"></i>
                        <p>{{item.popular.text}}</p>                      
                </div>
                <div class="d_flex mb_20">
                    <i :class="item.popular.icon"></i>
                    <p>{{item.popular.text}}</p>  
                </div>
                <div class="d_flex mb_20">
                    <i :class="item.popular.icon"></i>
                    <p>{{item.popular.text}}</p>  
                </div>
                <div class="d_flex mb_20">
                    <i :class="item.popular.icon"></i>
                    <p>{{item.popular.text}}</p>  
                </div>                
            </div>

            <div>
                <h4 class="mb_20">{{item.recent.title}}</h4>
                <div class="d_flex mb_20">
                    <i :class="item.recent.icon"></i>
                    <p>{{item.recent.text}}</p>  
                </div>
                <div class="d_flex mb_20">
                    <i :class="item.recent.icon"></i>
                    <p>{{item.recent.text}}</p>  
                </div>
                <div class="d_flex mb_20">
                    <i :class="item.recent.icon"></i>
                    <p>{{item.recent.text}}</p>  
                </div>
                <div class="d_flex mb_20">
                    <i :class="item.recent.icon"></i>
                    <p>{{item.recent.text}}</p>  
                </div>
            </div>

            <div>
                <h4 class="mb_20 mb_20">{{item.latest.title}}</h4>
                <div class="d_flex mb_20">
                    <i :class="item.latest.icon"></i>
                    <p>{{item.latest.text}}</p>  
                </div>
                <div class="d_flex mb_20">
                    <i :class="item.latest.icon"></i>
                    <p>{{item.latest.text}}</p>  
                </div>
                <div class="d_flex mb_20">
                    <i :class="item.latest.icon"></i>
                    <p>{{item.latest.text}}</p>  
                </div>
                <div class="d_flex mb_20">
                    <i :class="item.latest.icon"></i>
                    <p>{{item.latest.text}}</p>  
                </div>
            </div>          
        </div>   
    </div>
</template>

<script>
    export default {
        name: 'MyFooterLinks',
        props: {
            shareData: Array,
        }
    }
</script>

<style lang="scss">
    .links_container {
        align-items: center;
    }
</style>