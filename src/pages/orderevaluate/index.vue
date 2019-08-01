<template>
<div class="orderPage">
    <div class="box"><img src="/static/images/evaluate-1.png" alt=""></div>
    <div class="btn">发表评价</div>
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
      targetUrl (param) {
        const _url = '/pages/' + param + '/main'
        mpvue.navigateTo({'url': _url})
      }
    }
  }
</script>

<style scoped>
.orderPage{
    background: rgb(247,247,247);
    width: 100%;
    height: 100%;
    position: absolute;
}
.orderPage .box{
    width: 100%;
    margin-top: 10px;
    overflow: hidden;
}
.orderPage .box img{
    width: 750rpx;
    height: 758rpx;
}
.orderPage .btn{
    width:640rpx;
    line-height:80rpx;
    color: #fff;
    font-size:36rpx;
    margin: 0 auto;
    text-align: center;
    border-radius:10rpx;
    left: 55rpx;
    bottom: 40rpx;
    position: absolute;
    background:#C79F62;
}
</style>
