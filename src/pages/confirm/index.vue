<template>
<div class="container confirmPage">
    <div class="confirmBd">
        <div class="group confirm-1"><img src="/static/images/confirm-1.png" alt=""></div>
        <div class="group confirm-2"><img src="/static/images/confirm-2.png" alt=""></div>
        <div class="group confirm-3"><img src="/static/images/confirm-3.png" alt=""></div>
        <div class="group confirm-4"><img src="/static/images/confirm-4.png" alt=""></div>
    </div>
    <div class="buy-cart">
        <div class="cart-bd">
            <div class="info">
                <dl>
                    <dt>￥109</dt>
                    <dd>支付</dd>
                </dl>
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
    }
  }
</script>

<style scoped>
.confirmPage{
    background: #f8f9f7;
}
.confirmBd{
    width: 100%;
    /*display:flex;*/
    /*flex:1;*/
    padding-bottom:100rpx;
    overflow:hidden;
}
.confirmBd .group{
    margin-bottom: 10px;
}
.confirmBd .group img{
    width: 750rpx;
    display: block;
}
.confirm-1 img{
    height: 436rpx;
}
.confirm-2 img{
    height: 422rpx;
}
.confirm-3 img{
    height: 270rpx;
}
.confirm-4 img{
    height: 176rpx;
}
.buy-cart{
    clear: both;
    position: fixed;
    background-color: #F2F2F2;
    bottom: 0;
    left: 0;
    z-index: 13;
    display: flex;
    width: 100%;
    height: 50px;
}
.cart-bd{
    flex: 1;
}
.cart-bd .info dt{
    float: left;
    padding: 0 15px;
    line-height: 50px;
}
.cart-bd .info dd{
    float: right;
    background: #C79F62;
    color: #fff;
    line-height: 50px;
    width: 100px;
    text-align: center;
}
</style>
