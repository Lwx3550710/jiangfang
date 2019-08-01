<template>
    <div class="diningwayPage">
        <div class="photo"><img src="/static/images/diningway-1.png" alt=""></div>
    </div>
</template>

<script>
  // Use Vuex
  import store from './store'

  export default {
    data () {
      return {
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
    .diningwayPage{
        background: rgb(247,247,247);
        width: 100%;
        height: 100%;
        position: absolute;
    }
    .diningwayPage .photo img{
        width: 750rpx;
        height: 430rpx;
    }
</style>
