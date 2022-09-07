<template>
  <div id="app">
    <div class="turn_back" @click="goto('top')"><i class="fa-solid fa-angle-up"></i></div>
    <MyHeader ref="top"/>
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
  methods: {
    goto(refName) {
      let element = this.$refs[refName];
      let top = element.offsetTop;
      window.scrollTo(0, top);
    }
  }
}
</script>

<style lang="scss">
  @import '@/styles/general.scss';

  .turn_back {
    height: 20px;
    width: 35px;
    background-color: $brand-color-black;
    border: 1px solid white;
    border-top-right-radius: 5px;
    border-top-left-radius: 5px;
    position: fixed;
    bottom: 0;
    right: 50px;
    z-index: 998;
    color: white;
    text-align: center;
    cursor: pointer;
  }
</style>
