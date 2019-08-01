<template>
<div class="orderPage">
    <div class="group">
        <div class="userPhoto"><img src="/static/images/order-logo.png" alt=""></div>
        <div class="orderInfo">
            <div class="hd" @click="targetUrl('orderdetail')">
                <div class="store">
                    <p class="name">匠方肉夹馍(银泰店) <img src="/static/images/aw-r.png" alt=""></p>
                    <p class="time">2019-05-28 11:00</p>
                </div>
                <div class="status">待接单</div>
            </div>
            <div class="bd" @click="targetUrl('orderdetail')">
                <span>￥19</span>
                <p>这里是订单食物的名称</p>
            </div>
            <div class="ft">
                <span class="cancel" @click="targetUrl('orderevaluate')">取消订单</span>
            </div>
        </div>
    </div>
    <div class="group">
        <div class="userPhoto"><img src="/static/images/order-logo.png" alt=""></div>
        <div class="orderInfo">
            <div class="hd" @click="targetUrl('orderdetail')">
                <div class="store">
                    <p class="name">匠方肉夹馍(银泰店) <img src="/static/images/aw-r.png" alt=""></p>
                    <p class="time">2019-05-28 11:00</p>
                </div>
                <div class="status">待取餐</div>
            </div>
            <div class="bd" @click="targetUrl('orderdetail')">
                <span>￥19</span>
                <p>这里是订单食物的名称</p>
            </div>
            <div class="ft">
                <span class="confirm" @click="targetUrl('orderevaluate')">确认取餐</span>
            </div>
        </div>
    </div>
    <div class="group">
        <div class="userPhoto"><img src="/static/images/order-logo.png" alt=""></div>
        <div class="orderInfo">
            <div class="hd" @click="targetUrl('orderdetail')">
                <div class="store">
                    <p class="name">匠方肉夹馍(银泰店) <img src="/static/images/aw-r.png" alt=""></p>
                    <p class="time">2019-05-28 11:00</p>
                </div>
                <div class="status">已完成</div>
            </div>
            <div class="bd" @click="targetUrl('orderdetail')">
                <span>￥19</span>
                <p>这里是订单食物的名称</p>
            </div>
            <div class="ft">
                <span class="confirm" @click="targetUrl('orderevaluate')">再来一单</span>
                <span class="pingjia" @click="targetUrl('orderevaluate')">评价</span>
            </div>
        </div>
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
.orderPage .group{
    clear: both;
    background: #fff;
    display: flex;
    padding: 0 10px;
    flex: 1;
    margin-bottom: 10px;
    overflow: hidden;
}
.orderPage .userPhoto,.orderPage .userPhoto img{
    width: 70rpx;
    height: 70rpx;
}
.orderPage .userPhoto{
    padding: 10px 0;
}
.orderPage .orderInfo{
    margin-left: 10px;
    flex: 1;
    overflow: hidden;
}
.orderPage .orderInfo .hd{
    width: 100%;
    clear: both;
    padding: 8px 0;
    overflow: hidden;
}
.orderPage .orderInfo .hd .store{
    width: 70%;
    float: left;
}
.orderPage .orderInfo .hd .name{
    font-size:30rpx;
    color:rgba(0,0,0,1);
    line-height:40rpx;
}
.orderPage .orderInfo .hd .time{
    font-size:24rpx;
    color:rgba(153,153,153,1);
    line-height:40rpx;
}
.orderPage .orderInfo .hd .name img{
    width: 20rpx;
    height: 20rpx;
}
.orderPage .orderInfo .hd .status{
    color: #C79F62;
    font-size: 28rpx;
    line-height: 80rpx;
    float: right;
}
.orderPage .orderInfo .bd{
    padding: 15px 0;
    border-top: 1px #E6E6E6 solid;
    border-bottom: 1px #E6E6E6 solid;
    overflow: hidden;
}
.orderPage .orderInfo .bd p{
    width: 80%;
    color: #333333;
    font-size: 28rpx;
    float: left;
}
.orderPage .orderInfo .bd span{
    float: right;
}
.orderPage .group .ft{
    width: 100%;
    padding: 10px 0;
    text-align: right;
    overflow: hidden;
}
.orderPage .group .ft span{
    width:120rpx;
    height:36rpx;
    color:#666;
    font-size: 24rpx;
    display: inline-block;
    text-align: center;
    background:rgba(255,255,255,1);
    border:1px solid rgba(218,218,218,1);
    border-radius:6rpx;
    margin-left: 10px;
}
.orderPage .group .ft .cancel{
    color:#666;
}
.orderPage .group .ft .confirm{
    color:#C79F62;
    border-color: #C79F62;
}
.orderPage .group .ft .pingjia{
    color:#E50110;
    border-color: #E50110;
}
</style>
