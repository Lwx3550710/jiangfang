<template>
<div class="orderPage">
    <div class="box"><img src="/static/images/orderdetail.png" alt=""></div>
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
.orderPage .box{
    width: 100%;
    margin-top: 10px;
    overflow: hidden;
}
.orderPage .box img{
    width: 750rpx;
    height: 1645rpx;
}
</style>
