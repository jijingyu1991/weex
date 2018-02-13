<template>
  <div class="wrapper">
    <top-header></top-header>
    <div>
      <input type="text" placeholder="请输入" class="textInput">
    </div>
    <image :src="logo" class="logo"></image>
    <text class="greeting">The environment is ready!</text>
    <text class="message">Now, let's use Vue.js to build your Weex apps.</text>
  </div>
</template>

<script>
import topHeader from './topHeader.vue'
var modal = weex.requireModule('modal')
  export default {
    components:{
      topHeader
    },
    created () {
      modal.toast({
        message: '页面初始化成功',
        duration: 3
      })
    },
    data () {
      return {
        logo: 'https://gw.alicdn.com/tfs/TB1yopEdgoQMeJjy1XaXXcSsFXa-640-302.png',
      }
    }
  }
</script>

<style scoped>
  .wrapper {
    /* justify-content: center; */
    /* align-items: center; */
  }
  .logo {
    width: 424px;
    height: 200px;
  }
  .greeting {
    font-size: 50px;
    color: #41B883;
  }
  .message {
    margin: 30px;
    font-size: 32px;
    color: #727272;
  }

  .textInput{
    height:80px; 
    padding:10px;
    font-size:32px; 
    width:750px;
    border-bottom-width:1px;
  }
</style>
