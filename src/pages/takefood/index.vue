<template>
  <div class="container">
      <div class="card-main">
          <div class="body">
              <div class="title">堂食</div>
              <div class="process">
                  <div class="no">JF009</div>
                  <div class="jd">您的餐品正在制作中</div>
                  <div class="store"><b>匠方银泰城店</b><img src="/static/takefood/aw.png"/></div>
              </div>
              <div class="info">
                  <div class="item">
                      <div class="box1">
                          <div class="name">商品信息名称</div>
                          <div class="price">￥12</div>
                          <div class="spec">x1</div>
                      </div>
                      <div class="box2">口味内容</div>
                  </div>
                  <div class="item">
                      <div class="box1">
                          <div class="name">商品信息名称</div>
                          <div class="price">￥12</div>
                          <div class="spec">x1</div>
                      </div>
                      <div class="box2">口味内容</div>
                  </div>
                  <div class="more">
                      <dl>
                          <dt>查看其余3件</dt>
                          <dd><img src="/static/takefood/aw-cur.png" alt=""></dd>
                      </dl>
                  </div>
              </div>
              <div class="total">
                  <dl>
                      <dt>总计</dt>
                      <dd>￥60</dd>
                  </dl>
              </div>
          </div>
          <div class="bg"><img src="/static/takefood/card-bg.png" alt=""></div>
      </div>
    <div class="copyright">注:请注意前台叫号，您也可以通过刷新小程序<br>查看取餐进度</div>
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
    increment () {
      store.commit('increment')
    },
    decrement () {
      store.commit('decrement')
    }
  }
}
</script>

<style scoped>
.container{
    background: #F8F9F7;
    width: 100%;
    position: absolute;
}
.card-main{
    width: 323px;
    height: 480px;
    position: relative;
    z-index: 1;
    margin: 15px auto 0;
    overflow: hidden;
}
.card-main .body{
    position: absolute;
    z-index: 2;
    width: 100%;
    height: 100%;
}
.card-main .title{
    line-height: 93px;
    text-align: center;
    font-size: 20px;
}
.card-main .process{
    text-align: center;
    padding: 10px 0;
    overflow: hidden;
}
.card-main .process .no{
    color: #C79F62;
    font-size: 45px;
    line-height: 60px;
}
.card-main .process .jd{
    color: #000;
    font-size: 15px;
    line-height: 30px;
}
.card-main .process .store{
    color: #000;
    font-size: 16px;
    line-height: 30px;
}
.card-main .process .store b{
    display: inline-block;
    margin-right: 3px;
}
.card-main .process .store img{
    width: 10px;
    height: 10px;
}
.card-main .info{
    padding: 0 20px;
    overflow: hidden;
}
.card-main .info .item{
    width: 100%;
    margin-top: 15px;
    overflow: hidden;
}
.card-main .info .item .box1{
    line-height: 30px;
}
.card-main .info .item .box1 .name{
    color: #000;
    font-size: 15px;
    float: left;
}
.card-main .info .item .box1 .spec{
    color: #666;
    font-size: 12px;
    float: right;
    margin-right: 15px;
}
.card-main .info .item .box1 .price{
    color: #000;
    font-size: 15px;
    float: right;
}
.card-main .info .item .box2{
    color: #666;
    font-size: 12px;
    line-height: 20px;
    clear: both;
}
.card-main .info .item:last-child{
    margin-bottom: 0;
}
.card-main .info .more{
    width: 100%;
    line-height: 40px;
    margin:5px 0 10px;
    overflow: hidden;
}
.card-main .info .more dt{
    color: #C79F62;
    font-size: 13px;
    float: left;
}
.card-main .info .more dd{
    float: right;
    width: 9px;
    height: 9px;
}
.card-main .info .more dd img{
    width: 9px;
    height: 9px;
}
.card-main .total{
    margin: 0 20px;
    border-top: 1px #ccc dashed;
    overflow: hidden;
}
.card-main .total dt{
    font-size: 14px;
    line-height: 60px;
    float: left;
}
.card-main .total dd{
    font-size: 18px;
    line-height: 60px;
    font-weight: bold;
    float: right;
}
.card-main .bg{
    position: absolute;
    z-index: 1;
    width: 100%;
    height: 100%;
}
.card-main .bg img{
    width: 100%;
    height: 100%;
}
.copyright{
    color: #999;
    font-size: 12px;
    text-align: center;
    padding: 15px 0;
}
</style>
