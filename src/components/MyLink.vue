<template>
    <div>
        <div v-for="(obj, index) in array" :key="index">
            <h4>{{obj.title}}</h4>
            <i :class="obj.icon"></i>
            <p>{{obj.text}}</p>                      
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

<style>

</style>