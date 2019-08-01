<template>
    <div class="tradePage">
        <div class="title">请再次输入</div>
        <div class="group">
            <div class="items"><input type="text"></div>
            <div class="items"><input type="text"></div>
            <div class="items"><input type="text"></div>
            <div class="items"><input type="text"></div>
            <div class="items"><input type="text"></div>
            <div class="items"><input type="text"></div>
        </div>
        <div class="h-60"></div>
        <div class="btn">保存密码</div>
    </div>
</template>

<script>
  // Use Vuex
  import store from './store'

  export default {
    data () {
      return {
        list: [{
          'money': '59'
        }, {
          'money': '23'
        }, {
          'money': '534'
        }, {
          'money': '343'
        }]
      }
    },
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
    .tradePage{
        padding: 15px;
        overflow: hidden;
    }
    .title{
        font-size:36rpx;
        font-weight:500;
        color:rgba(0,0,0,1);
        line-height:50px;
        padding: 0 20px;
    }
    .tradePage .group{
        padding: 20px 0;
        clear: both;
        text-align: center;
        overflow: hidden;
    }
    .tradePage .group .items{
        width:80rpx;
        height:80rpx;
        background:rgba(255,255,255,1);
        margin: 0 5px;
        display: inline-block;
        border:1px solid rgba(153,153,153,1);
    }
    .tradePage .group .items input{
        width:80rpx;
        line-height:80rpx;
        height:80rpx;
    }
    .tradePage .btn{
        width:640rpx;
        line-height:80rpx;
        color: #fff;
        font-size:36rpx;
        margin: 0 auto;
        border-radius:10rpx;
        text-align: center;
        background:#C79F62;
    }
    .h-60{
        height: 140px;
    }
</style>
