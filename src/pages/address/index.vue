<template>
<div class="addressPage">
    <div class="group"><img src="/static/images/address-1.png"></div>
    <div class="btn" @click="tjAddress">添加地址</div>
</div>
</template>

<script>
  // Use Vuex
  import store from './store'

  export default {
    computed: {
      count () {
        return store.state.count
      }
    },
    methods: {
      tjAddress () {
        mpvue.navigateTo({'url': '/pages/add-address/main'})
      }
    }
  }
</script>

<style scoped>
.addressPage{
    background: rgb(247,247,247);
    width: 100%;
    height: 100%;
    position: absolute;
}
.addressPage img{
    width: 750rpx;
    height: 157rpx;
    display: block;
}
.addressPage .btn{
    width:640rpx;
    line-height:80rpx;
    color: #fff;
    font-size:36rpx;
    margin: 0 auto;
    border-radius:10rpx;
    left: 55rpx;
    bottom: 40rpx;
    text-align: center;
    position: absolute;
    background:rgba(38,30,19,1);
}
</style>
