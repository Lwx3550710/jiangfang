<template>
  <div class="counter-warp">
    <div class="mod-hd">
        <div class="user">
            <div class="photo" @click="targetUrl('myinfo')"><img src="/static/my/per-default.png"></div>
            <div class="info">
                <div class="name">这里是用户</div>
                <div class="btn">点击授权</div>
            </div>
        </div>
        <div class="assets">
            <div class="items">
                <b>29</b>
                <span>积分</span>
            </div>
            <div class="items" @click="targetUrl('coupons')">
                <b>5</b>
                <span>我的券</span>
            </div>
            <div class="items" @click="targetUrl('redpacket')">
                <b>0</b>
                <span>我的红包</span>
            </div>
            <div class="items" @click="targetUrl('wallet')">
                <b>29</b>
                <span>钱包</span>
            </div>
        </div>
    </div>
    <div class="mod-group">
      <div class="items" v-for="items in group" @click="targetUrl(items.target)">
          <img :src="items.icon" class="icon">
          <b class="title">{{items.title}}</b>
          <img src="/static/my/arrow.png" class="arrow">
      </div>
    </div>
  </div>
</template>

<script>
// Use Vuex
import store from './store'

export default {
  data () {
    return {
      userInfo: {
        nickName: 'mpvue',
        avatarUrl: 'http://mpvue.com/assets/logo.png'
      },
      group: [{
        'title': '收货地址',
        'icon': '/static/my/address.png',
        'target': 'address'
      }, {
        'title': '我的订单',
        'icon': '/static/my/order.png',
        'target': 'orderlist'
      }, {
        'title': '我的会员',
        'icon': '/static/my/member.png',
        'target': 'member'
      }, {
        'title': '邀请好友',
        'icon': '/static/my/invite.png',
        'target': 'invite'
      }, {
        'title': '在线客服',
        'icon': '/static/my/kf.png',
        'target': 'kf'
      }, {
        'title': '意见反馈',
        'icon': '/static/my/idea.png',
        'target': 'idea'
      }, {
        'title': '关于匠方',
        'icon': '/static/my/about.png',
        'target': 'about'
      }, {
        'title': '投资人/经营人',
        'icon': '/static/my/invest.png',
        'target': 'invest'
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
      // console.log(param)
      const _url = '/pages/' + param + '/main'
      mpvue.navigateTo({'url': _url})
    }
  }
}
</script>

<style scoped>
.mod-hd{
    background: rgb(246, 246, 246);
    width: 100%;
    min-height: 100px;
    overflow: hidden;
}
.mod-hd .user{
    padding: 20px;
    clear: both;
    overflow: hidden;
}
.mod-hd .user .photo{
    float: left;
    width: 60px;
    margin-right: 15px;
}
.mod-hd .user .photo img{
    width: 60px;
    height: 60px;
}
.mod-hd .user .info{
    float: left;
}
.mod-hd .user .info .name{
    font-size: 18px;
    color: #000;
    line-height: 30px;
    font-weight: bold;
}
.mod-hd .user .info .btn{
    line-height: 22px;
    background: #040404;
    color: #fff;
    padding: 0 10px;
    border-radius: 20px;
    display: inline-block;
    text-align: center;
}
.mod-hd .assets{
    clear: both;
    display: flex;
}
.mod-hd .assets .items{
    flex: 1;
    text-align: center;
    padding: 15px 0;
}
.mod-hd .assets .items b{
    font-size: 24px;
    color: #000;
}
.mod-hd .assets .items span{
    font-size: 12px;
    color: #000;
}
.mod-group {
    width: 100%;
    clear: both;
    overflow: hidden;
}
.mod-group .items{
    padding: 10px 15px;
    clear: both;
    overflow: hidden;
}
.mod-group .items .icon{
    width: 20px;
    height: 20px;
    float: left;
    margin: 5px 10px 0 0;
}
.mod-group .items .title{
    float: left;
    line-height: 30px;
    color: #333;
    font-size: 14px;
}
.mod-group .items .arrow{
    width: 15px;
    height: 15px;
    opacity: .3;
    float: right;
    margin-top: 7px;
    transform: rotate(-180deg);
}
</style>
