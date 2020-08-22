<template>
  <view class="container">
   
    <Home/>
  </view>
</template>

<script>
import Vuex from 'vuex';
import Vue from 'vue-native-core';
import store from "./src/store";
Vue.prototype.$store = store;
import Home from './src/screens/Home.vue';
export default {
  components: {
      Home
    },
}
</script>
<style>
.container {
  background-color: white;
  align-items: center;
  justify-content: center;
  flex: 1;
}
.text-color-primary {
  color: blue;
}
</style>
