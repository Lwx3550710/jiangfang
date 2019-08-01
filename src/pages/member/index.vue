<template>
<div class="memberPage">
    <div class="group"><img src="/static/images/member-bg.png"></div>
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
.memberPage img{
    width: 750rpx;
    height: 1205rpx;
    display: block;
}
</style>
