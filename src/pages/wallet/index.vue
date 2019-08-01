<template>
    <div class="container">
        <div class="hd">
            <div class="logo"><img src="/static/images/qb-hyk.png" alt=""></div>
            <div class="money">
                <dl>
                    <dt>可用余额</dt>
                    <dd>0</dd>
                </dl>
            </div>
            <div class="btn" @click="targetUrl('recharge')">立即充值</div>
        </div>
        <div class="group" v-for="items in list"  @click="targetUrl(items.target)">
            <b>{{items.name}}</b>
            <span><img src="/static/my/arrow.png" class="arrow"></span>
        </div>
    </div>
</template>

<script>
  // Use Vuex
  import store from './store'

  export default {
    data () {
      return {
        list: [{
          'name': '消费记录',
          'target': ''
        }, {
          'name': '修改交易密码',
          'target': 'tradepinone'
        }, {
          'name': '重置交易密码',
          'target': ''
        }]
      }
    },
    computed: {
      count () {
        return store.state.count
      }
    },
    methods: {
      targetUrl (param) {
        if (param) {
          const _url = '/pages/' + param + '/main'
          mpvue.navigateTo({'url': _url})
        }
      }
    }
  }
</script>

<style scoped>
    .container{
        padding: 15px;
        overflow: hidden;
    }
    .hd{
        width: 100%;
        clear: both;
        margin: 0 auto;
        padding: 20px 0;
        border-bottom: 1px #E6E6E6 solid;
        overflow: hidden;
    }
    .hd .logo img{
        width: 500rpx;
        height: 300rpx;
        display: block;
        margin: 0 auto;
    }
    .hd dl{
        text-align: center;
        margin: 10px auto;
        overflow: hidden;
    }
    .hd dt{
        font-size:26rpx;
        line-height: 40px;
    }
    .hd dd{
        font-size: 24px;
        color: #000;
        font-weight: bold;
        line-height: 30px;
    }
    .hd dd:before{
        content: '￥';
        font-size: 12px;
        font-weight: normal;
    }
    .hd .btn{
        width:240rpx;
        line-height:80rpx;
        font-size: 18px;
        text-align: center;
        color: #fff;
        margin: 0 auto;
        background:rgba(38,30,19,1);
        border-radius:10rpx;
    }
    .group{
        line-height: 50px;
        width: 100%;
        border-bottom: 1rpx #E6E6E6 solid;
    }
    .group b{
        font-size:30rpx;
        color: #333;
        float: left;
    }
    .group .arrow{
        width: 15px;
        height: 15px;
        opacity: .3;
        float: right;
        margin-top: 19px;
        transform: rotate(-180deg);
    }
</style>
