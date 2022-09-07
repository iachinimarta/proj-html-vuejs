<template>
  <div id="app">
    <MyHeader/>
    <MyMain/>
    <MyFooter/>
  </div>
</template>

<script>
import MyHeader from './components/MyHeader.vue';
import MyMain from './components/Main/MyMain.vue';
import MyFooter from './components/Footer/MyFooter.vue';

export default {
  name: 'App',
  components: {
    MyHeader,
    MyMain,
    MyFooter,
  }, 
}
</script>

<style lang="scss">
   @import '@/styles/general.scss';
</style>
