<template>
<div class="ideaPage">
    <div class="box"><img src="/static/images/idea-1.png" alt=""></div>
    <div class="btn">提交反馈</div>
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
    }
  }
</script>

<style scoped>
.ideaPage{
    background: rgb(247,247,247);
    width: 100%;
    height: 100%;
    position: absolute;
}
.ideaPage .box img{
    width: 750rpx;
    height: 730rpx;
}
.ideaPage .btn{
    width:640rpx;
    line-height:80rpx;
    color: #fff;
    font-size:36rpx;
    margin: 20px auto;
    border-radius:10rpx;
    text-align: center;
    background:#C79F62;
}
</style>
