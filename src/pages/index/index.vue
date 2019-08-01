<template>
<div class="shop_container">
    <div class="header_bd">
        <div class="store">
            <span>匠方银泰城店</span>
            <img src="/static/takefood/aw.png" class="icon-1" alt="">
        </div>
        <div class="waimai" @click="targetUrl('diningway')">
            <img src="/static/home/waimai.png" class="icon-1" alt="">
            <span>外卖</span>
            <img src="/static/home/arrow.png" class="icon-2" alt="">
        </div>
        <div class="address"><img src="/static/home/address.png" alt="">距您500m</div>
    </div>
    <div class="food_bd">
        <div class="menu_bd">
            <ul>
                <li class="active">热销</li>
                <li>优惠</li>
                <li>口味1</li>
                <li>口味2</li>
                <li>口味3</li>
                <li>口味4</li>
            </ul>
        </div>
        <div class="wrapper_bd">
            <div class="photo"><img src="/static/home/adv.png" alt=""></div>
            <div class="items">
                <div class="food-img"><img src="//elm.cangdu.org/img/16772d91c1823153.jpg" alt=""></div>
                <div class="food-info">
                    <div class="name">驴肉火烧</div>
                    <div class="desc">来自西安地道的驴肉火烧 制作手艺传 承22年 好吃不贵！</div>
                    <div class="price">
                        <b>￥4.85</b>
                        <span>¥4.85</span>
                        <em>选规格</em>
                    </div>
                </div>
            </div>
            <div class="items">
                <div class="food-img"><img src="//elm.cangdu.org/img/16772d91c1823153.jpg" alt=""></div>
                <div class="food-info">
                    <div class="name">驴肉火烧</div>
                    <div class="desc">来自西安地道的驴肉火烧 制作手艺传 承22年 好吃不贵！</div>
                    <div class="price">
                        <b>￥4.85</b>
                        <span>¥4.85</span>
                        <em>选规格</em>
                    </div>
                </div>
            </div>
            <div class="items">
                <div class="food-img"><img src="//elm.cangdu.org/img/16772d91c1823153.jpg" alt=""></div>
                <div class="food-info">
                    <div class="name">驴肉火烧</div>
                    <div class="desc">来自西安地道的驴肉火烧 制作手艺传 承22年 好吃不贵！</div>
                    <div class="price">
                        <b>￥4.85</b>
                        <span>¥4.85</span>
                        <em>选规格</em>
                    </div>
                </div>
            </div>
            <div class="items">
                <div class="food-img"><img src="//elm.cangdu.org/img/16772d91c1823153.jpg" alt=""></div>
                <div class="food-info">
                    <div class="name">驴肉火烧</div>
                    <div class="desc">来自西安地道的驴肉火烧 制作手艺传 承22年 好吃不贵！</div>
                    <div class="price">
                        <b>￥4.85</b>
                        <span>¥4.85</span>
                        <em>选规格</em>
                    </div>
                </div>
            </div>
            <div class="items">
                <div class="food-img"><img src="//elm.cangdu.org/img/16772d91c1823153.jpg" alt=""></div>
                <div class="food-info">
                    <div class="name">驴肉火烧</div>
                    <div class="desc">来自西安地道的驴肉火烧 制作手艺传 承22年 好吃不贵！</div>
                    <div class="price">
                        <b>￥4.85</b>
                        <span>¥4.85</span>
                        <em>选规格</em>
                    </div>
                </div>
            </div>
            <div class="items">
                <div class="food-img"><img src="//elm.cangdu.org/img/16772d91c1823153.jpg" alt=""></div>
                <div class="food-info">
                    <div class="name">驴肉火烧</div>
                    <div class="desc">来自西安地道的驴肉火烧 制作手艺传 承22年 好吃不贵！</div>
                    <div class="price">
                        <b>￥4.85</b>
                        <span>¥4.85</span>
                        <em>选规格</em>
                    </div>
                </div>
            </div>
        </div>
    </div>
    <div class="buy-cart">
        <div class="cart-bd">
            <div class="btn">
                <div class="wrap">
                    <div class="txt"><img src="/static/home/cart.png" alt="">购物袋</div>
                    <div class="num">5</div>
                </div>
            </div>
            <div class="info">
                <dl>
                    <dt>￥109</dt>
                    <dd @click="targetUrl('confirm')">结算</dd>
                </dl>
            </div>
        </div>
    </div>
</div>

</template>

<script>
import card from '@/components/card'

export default {
  data () {
    return {
      motto: '',
      userInfo: {
        nickName: 'mpvue',
        avatarUrl: 'http://mpvue.com/assets/logo.png'
      }
    }
  },

  components: {
    card
  },

  methods: {
    targetUrl (param) {
      const _url = '/pages/' + param + '/main'
      mpvue.navigateTo({'url': _url})
    }
  },

  created () {
    // let app = getApp()
  }
}
</script>

<style scoped>
.shop_container{
    position: absolute;
    display: flex;
    flex-direction: column;
    right: 0;
    left: 0;
    height: 100%;
}
.header_bd{
    padding: 0 15px;
}
.header_bd .store{
    float: left;
    line-height: 30px;
}
.header_bd .store span{
    font-size: 16px;
    color: #000;
    margin-right: 6px;
}
.header_bd .store img{
    transform: rotate(90deg);
    width: 10px;
    height: 10px;
}
.header_bd .waimai{
    float: right;
    line-height: 30px;
}
.header_bd .waimai span{
    color: #C79F62;
    padding: 0 5px;
}
.header_bd .waimai .icon-1{
    width: 32rpx;
    height: 30rpx;
}
.header_bd .waimai .icon-2{
    width: 10rpx;
    height: 16rpx;
}
.header_bd .address{
    clear: both;
    font-size: 11pxx;
    line-height: 30px;
    color: #666;
}
.header_bd .address img{
    width: 19rpx;
    height: 22rpx;
    margin-right: 6px;
}
.food_bd{
    display: flex;
    flex: 1;
    padding-bottom: 50px;
    overflow: hidden;
}
.menu_bd{
    width: 90px;
    background: #F7F7F7;
}
.menu_bd li{
    line-height: 60px;
    font-size: 14px;
    color: #999;
    text-align: center;
    padding: 0 5px;
}
.menu_bd li.active{
    border-left: .15rem solid #C79F62;
    background-color: #fff;
}
.wrapper_bd{
    flex: 4;
    padding: 10px;
    overflow-y: auto;
}
.wrapper_bd .photo img{
    width: 530rpx;
    height: 242rpx;
}
.wrapper_bd .items{
    width: 100%;
    clear: both;
    display: flex;
    overflow: hidden;
}
.wrapper_bd .items .food-img{
    width: 60px;
    margin-right: 10px;
}
.wrapper_bd .items .food-img img{
    width: 60px;
    height: 60px;
}
.wrapper_bd .items .food-info{
    width: 100%;
}
.wrapper_bd .items .food-info .name{
    font-size: 14px;
    line-height: 30px;
    color: #000;
}
.wrapper_bd .items .food-info .desc{
    color: #aaa;
    font-size: 11px;
    line-height: 14px;
}
.wrapper_bd .items .food-info .price b{
    font-size: 14px;
    color: #C79F62;
    line-height: 30px;
    display: inline-block;
    margin-right: 10px;
}
.wrapper_bd .items .food-info .price span{
    font-size: 10px;
    color: #ccc;
    line-height: 30px;
    display: inline-block;
}
.wrapper_bd .items .food-info .price em{
    display: inline-block;
    background: #C79F62;
    color: #fff;
    line-height: 20px;
    padding: 0 5px;
    border-radius: 20px;
    font-size: 11px;
    float: right;
    margin-top: 6px;
}
.buy-cart{
    clear: both;
    position: absolute;
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
.cart-bd .btn{
    position: absolute;
    top: -8px;
    left: 15px;
    width: 100px;
    height: 45px;
    border-radius: 30px;
    background: #fff;
    text-align: center;
    box-shadow:0 2px 10px 1px rgba(16,16,16,0.1);
}
.cart-bd .btn .wrap{
    flex: 1;
    position: relative;
}
.cart-bd .btn .wrap .txt{
    font-size: 15px;
    color: #000;
    line-height: 45px;
}
.cart-bd .btn .wrap .txt img{
    width: 15px;
    height: 18px;
    margin-right: 6px;
    vertical-align: text-top;
}
.cart-bd .btn .wrap .num{
    position: absolute;
    z-index: 2;
    width: 19px;
    height: 19px;
    line-height: 19px;
    top: 0;
    right: 5px;
    background: #C79F62;
    color: #fff;
    font-size: 11px;
    border-radius: 50%;
}
.cart-bd .info{
    float: right;
}
.cart-bd .info dt{
    float: left;
    padding: 0 15px;
    line-height: 50px;
}
.cart-bd .info dd{
    float: left;
    background: #C79F62;
    color: #fff;
    line-height: 50px;
    width: 100px;
    text-align: center;
}
</style>
