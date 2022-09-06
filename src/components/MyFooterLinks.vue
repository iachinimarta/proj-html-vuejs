<template>
    <div>
        <div v-for="(item, index) in shareData" :key="index" class="d_flex">
            <div>
                <h5>{{item.popular.title}}</h5>
                <div class="d_flex">
                    <i :class="item.popular.icon"></i>
                    <p>{{item.popular.text}}</p>  
                </div>
                <div class="d_flex">
                    <i :class="item.popular.icon"></i>
                    <p>{{item.popular.text}}</p>  
                </div>
                <div class="d_flex">
                    <i :class="item.popular.icon"></i>
                    <p>{{item.popular.text}}</p>  
                </div>
                <div class="d_flex">
                    <i :class="item.popular.icon"></i>
                    <p>{{item.popular.text}}</p>  
                </div>                
            </div>

            <div>
                <h5>{{item.recent.title}}</h5>
                <div class="d_flex">
                    <i :class="item.recent.icon"></i>
                    <p>{{item.recent.text}}</p>  
                </div>
                <div class="d_flex">
                    <i :class="item.recent.icon"></i>
                    <p>{{item.recent.text}}</p>  
                </div>
                <div class="d_flex">
                    <i :class="item.recent.icon"></i>
                    <p>{{item.recent.text}}</p>  
                </div>
                <div class="d_flex">
                    <i :class="item.recent.icon"></i>
                    <p>{{item.recent.text}}</p>  
                </div>
            </div>

            <div>
                <h5>{{item.latest.title}}</h5>
                <div class="d_flex">
                    <i :class="item.latest.icon"></i>
                    <p>{{item.latest.text}}</p>  
                </div>
                <div class="d_flex">
                    <i :class="item.latest.icon"></i>
                    <p>{{item.latest.text}}</p>  
                </div>
                <div class="d_flex">
                    <i :class="item.latest.icon"></i>
                    <p>{{item.latest.text}}</p>  
                </div>
                <div class="d_flex">
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
</style>