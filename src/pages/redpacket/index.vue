<template>
<div class="wrap">
    <!--<div class="group group-1">-->
        <!--<div class="info-1">-->
            <!--<b>¥ 20</b>-->
            <!--<span>会员专属红包</span>-->
        <!--</div>-->
        <!--<div class="info-2">-->
            <!--<b>满任意金额可用，不限制 使门店用</b>-->
            <!--<span>2019-08-12到期</span>-->
        <!--</div>-->
        <!--<div class="info-3"></div>-->
    <!--</div>-->
    <div class="items items-1"><img src="/static/images/redpacket-1.png" alt=""></div>
    <div class="items items-2"><img src="/static/images/redpacket-2.png" alt=""></div>
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
.wrap{
    background: rgb(247,247,247);
    width: 100%;
    height: 100%;
    position: absolute;
}
.items{
    width: 100%;
    margin-top: 20rpx;
}
.items img{
    width: 750rpx;
    display: block;
}
.items-1 img{
    height: 180rpx;
}
.items-2 img{
    height: 300rpx;
}
.group{
    width: 100%;
    height: 180rpx;
}
.group-1{
    background: #FFF1B6;
}
.info-1{
    width: 25%;
    text-align: center;
    float: left;
}
.info-2{
    width: 45%;
    text-align: center;
    float: left;
}
.info-3{
    width: 30%;
    text-align: center;
    float: left;
}
.info-1 b{
    font-size: 22px;
}
.info-1 span{
    font-size:22rpx;
    line-height:80rpx;
}
.info-2 b{
    font-size:14px;
    line-height:80rpx;
}
.group-1 .info-1 span{
    color:rgba(115,91,39,1);
}
</style>
