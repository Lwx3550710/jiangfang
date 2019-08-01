<template>
<div class="addressPage">
    <div class="info-bd">
        <dl>
            <dt><img src="/static/my/per-default.png" alt=""></dt>
            <dd>用户的微信名</dd>
        </dl>
    </div>
    <div class="ad-form">
        <div class="group">
            <div class="form-label">昵称</div>
            <div class="form-input"><input type="text" class="i-text" value="默认微信名"></div>
        </div>
        <div class="group">
            <div class="form-label">手机号</div>
            <div class="form-input"><input type="text" class="i-text" value="13920191234"></div>
        </div>
        <div class="group">
            <div class="form-label">性别</div>
            <div class="form-input">
                <label for="sex1"><input type="radio" name="sex" id="sex1" checked>男士</label>
                <label for="sex2"><input type="radio" name="sex" id="sex2">女士</label>
            </div>
        </div>
        <div class="group">
            <div class="form-label">生日</div>
            <div class="form-input"><input type="text" class="i-text"></div>
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
.addressPage{
    background: rgb(247,247,247);
    width: 100%;
    height: 100%;
    position: absolute;
}
.info-bd{
    background: #fff;
    width: 100%;
    height: 180px;
    display: flex;
}
.info-bd dl{
    flex: 1;
    text-align: center;
    padding: 35px 0;
}
.info-bd dt img{
    width: 150rpx;
    height: 150rpx;
    display: block;
    margin: 0 auto;
}
.info-bd dd{
    line-height: 40px;
}
.addressPage .ad-form{
    width: 750rpx;
    background: #fff;
    margin: 10px 0;
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
