<template>
    <div>
        <div v-for="(obj, index) in array" :key="index" class="links_container">
            <h4 class="mb_20">{{obj.title}}</h4>      
            <a href="#">
                <i :class="obj.icon"></i>
                {{obj.text.a}}
            </a>
            <a href="#">
                <i :class="obj.icon"></i>
                {{obj.text.b}}
            </a>
            <a href="#">
                <i :class="obj.icon"></i>
                {{obj.text.c}}
            </a>
            <a href="#">
                <i :class="obj.icon"></i>
                {{obj.text.d}}
            </a>                     
        </div>
    </div>
</template>

<script>
    export default {
        name: 'MyLink',
        props: {
            array: Array
        },
    }
</script>

<style lang="scss">
    .links_container {
        margin: 0 20px;

        a {
            display: block;
            margin-bottom: 15px;
        }
    }
</style>