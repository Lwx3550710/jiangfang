<template>
    <div class="rechargePage">
        <div class="title">请选择充值金额</div>
        <div class="group">
            <div class="items" :class="key==0 ? 'active' : ''" v-for="(items, key) in list">
                <div class="money">￥{{items.money}}</div>
                <div class="bg" v-if="key == 0"><img src="/static/images/recharge-2.png" alt=""></div>
                <div class="bg" v-else><img src="/static/images/recharge-1.png" alt=""></div>
            </div>
        </div>
        <div class="btn">立即充值</div>
        <div class="foot"><img src="/static/images/recharge-3.png" alt=""></div>
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
    .rechargePage{
        padding: 15px;
        overflow: hidden;
    }
    .title{
        font-size:36rpx;
        font-weight:500;
        color:rgba(0,0,0,1);
        line-height:50px;
    }
    .rechargePage .group{
        padding-bottom: 40px;
        clear: both;
        overflow: hidden;
    }
    .rechargePage .group .items{
        width: 150px;
        height: 75px;
        position: relative;
        z-index: 1;
        float: left;
        margin: 10px;
        overflow: hidden;
    }
    .rechargePage .group .items:nth-child(odd){
        margin-right: 15px;
    }
    .rechargePage .group .items div{
        width: 150px;
        height: 75px;
        text-align: center;
        position: absolute;
    }
    .rechargePage .group .items .money{
        z-index: 2;
        font-size: 20px;
        color: #C79F62;
        line-height: 75px;
    }
    .rechargePage .group .items.active .money{
        color: #fff;
    }
    .rechargePage .group .items .bg{
        z-index: 1;
    }
    .rechargePage .group .items img{
        width: 150px;
        height: 75px;
    }
    .rechargePage .btn{
        width:640rpx;
        line-height:80rpx;
        color: #fff;
        font-size:36rpx;
        margin: 0 auto;
        border-radius:10rpx;
        text-align: center;
        background:#C79F62;
    }
    .rechargePage .foot{
        width: 100%;
        clear: both;
        padding: 20px 0;
    }
    .rechargePage .foot img{
        width: 418rpx;
        height: 402rpx;
        display: block;
        margin: 0 auto;
    }
</style>
