<template>
    <div class="container">
        <img src="/static/my/kf-bg.png">
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
        background: #fff;
        width: 100%;
        position: absolute;
    }
    .container img{
        width: 100%;
        height: 100%;
    }
</style>
