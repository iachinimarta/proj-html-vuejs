<template>
  <div>
    <div v-for="(links, index) in shareData" :key="index" class="d_flex mt_20">
        <img  class="mr_20" :src="links.src" :alt="links.alt">
        <div>
            <a :href="links.link">
                <h4 class="mb_10">{{links.title}}</h4>
            </a>  
            <div class="d_flex fs_11">  
                <p>{{links.date}} |</p>
                <p v-if="links.active == false"> Comments Off</p>                 
            </div>
        </div>    
    </div>
  </div>
</template>

<script>
    export default {
        name: 'MyTutorialLinks',
        props: {
            shareData: Array
        }
    }
</script>

<style lang="scss">
@import '@/styles/general.scss';

</style>