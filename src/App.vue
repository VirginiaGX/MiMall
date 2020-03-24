<template>
  <div id="app">
    <router-view></router-view>
  </div>
</template>

<script>
// import jsonp from 'jsonp'
// import axios from 'axios'
// import storage from './storage/index.js'
export default {
  name: 'App',
  components: {
  },
  data () {
    return {
      res: {}
    }
  },
  methods:{
  getUser(){
    this.axios.get('/user').then(()=>{
      //to-do保存到vuex里面
    })
  },
  getCartCount(){
    this.axios.get('/carts/products/sum').then(()=>{
      //to-do保存到vuex里面
    })
  }
  },
  mounted (){
    this.getUser();
    this.getCartCount();
  }
 
}
</script>

<style lang='scss'>
@import './assets/scss/reset.scss';
@import './assets/scss/config.scss';
@import './assets/scss/button.scss';

</style>
