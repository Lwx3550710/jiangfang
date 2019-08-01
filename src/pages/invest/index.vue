<template>
  <div class="container">
    <div class="jf-box">
        <div class="jf-input"><input type="text" value="https://s?tn=news&rtt=1&bsst=.."></div>
        <div class="jf-btn"><button>复制</button></div>
    </div>
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
.container{
    background: #fff;
    width: 100%;
    position: absolute;
}
.jf-box{
    width:660rpx;
    height:90rpx;
    background:rgba(255,255,255);
    box-shadow:0 0 22rpx 0 rgba(40,40,40,0.1);
    border: 1rpx rgba(40,40,40,0.1) solid;
    border-radius:4rpx;
    margin: 188rpx auto;
    overflow: hidden;
}
.jf-input{
    width: 528rpx;
    height:90rpx;
    float: left;
}
.jf-input input{
    width: 508rpx;
    padding: 0 10rpx;
    line-height:90rpx;
    height:90rpx;
    font-size:30rpx;
}
.jf-btn{
    width:132rpx;
    height:90rpx;
    box-shadow:0 1rpx 22rpx 0 rgba(40,40,40,0.1);
    border-radius:4rpx;
    float: left;
}
.jf-btn button{
    width:132rpx;
    height:90rpx;
    color: #fff;
    font-size:30rpx;
    font-family:PingFang-SC-Medium;
    font-weight:bold;
    color:rgba(255,255,255,1);
    background:rgb(199,159,98);
}
</style>
