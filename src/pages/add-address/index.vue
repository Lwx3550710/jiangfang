<template>
<div class="addressPage">
    <div class="ad-form">
        <div class="group">
            <div class="form-label">联系人</div>
            <div class="form-input"><input type="text" class="i-text" value="李一"></div>
        </div>
        <div class="group">
            <div class="form-label"></div>
            <div class="form-input">
                <label for="sex1"><input type="radio" name="sex" id="sex1" checked>男士</label>
                <label for="sex2"><input type="radio" name="sex" id="sex2">女士</label>
            </div>
        </div>
        <div class="group">
            <div class="form-label">手机号</div>
            <div class="form-input"><input type="text" class="i-text" value="13920191234"></div>
        </div>
        <div class="group">
            <div class="form-label">收货地址</div>
            <div class="form-input"><input type="text" class="i-text" value="悠方购物中心"></div>
        </div>
        <div class="group">
            <div class="form-label">门牌号</div>
            <div class="form-input"><input type="text" class="i-text" value="写字楼A座2006室"></div>
        </div>
    </div>
    <div class="btn">保存</div>
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
.addressPage{
    background: rgb(247,247,247);
    width: 100%;
    height: 100%;
    position: absolute;
}
.addressPage .ad-form{
    width: 750rpx;
    background: #fff;
    margin: 25px 0;
    overflow: hidden;
}
.addressPage .group{
    width: 720rpx;
    padding: 0 15px;
    border-bottom: 1px #E6E6E6 solid;
    display: flex;
    flex: 1;
    overflow: hidden;
}
.addressPage .group .form-label{
    width: 80px;
    font-size: 15px;
    line-height: 50px;
    height: 50px;
}
.addressPage .group .form-input label{
    margin: 12px 15px 0 0;
    font-size: 15px;
    display: inline-block;
}
.addressPage .group .form-input .i-text{
    line-height: 50px;
    height: 50px;
    color: #999999;
}
.addressPage .btn{
    width:640rpx;
    line-height:80rpx;
    color: #fff;
    font-size:36rpx;
    margin: 0 auto;
    border-radius:10rpx;
    text-align: center;
    background:#C79F62;
}
</style>
