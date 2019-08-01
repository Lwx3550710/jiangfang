<template>
<div class="container">
    <div class="wrap">
        <div class="group"><img src="/static/images/coupons-1.png"></div>
        <div class="group"><img src="/static/images/coupons-2.png"></div>
        <div class="group"><img src="/static/images/coupons-2.png"></div>
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
.container{
    background: rgb(247,247,247);
    width: 100%;
    position: absolute;
}
.group{
    padding: 20px 20px 0;
}
.group img{
    width: 340px;
    height: 139px;
    display: block;
}
</style>
