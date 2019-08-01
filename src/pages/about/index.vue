<template>
  <div class="container">
      <div class="group" v-for="items in list">
          <b>{{items.name}}</b>
          <span><img src="/static/my/arrow.png" class="arrow"></span>
      </div>
  </div>
</template>

<script>
// Use Vuex
import store from './store'

export default {
  data () {
    return {
      list: [{
        'name': '匠方文化'
      }, {
        'name': '匠方隐私保护政策'
      }, {
        'name': '加盟匠方'
      }, {
        'name': '钱包章程'
      }, {
        'name': '常见问题'
      }]
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
.container{
    padding: 15px;
    overflow: hidden;
}
.group{
    line-height: 50px;
    width: 100%;
    border-bottom: 1rpx #E6E6E6 solid;
}
.group b{
    font-size:30rpx;
    color: #333;
    float: left;
}
.group .arrow{
    width: 15px;
    height: 15px;
    opacity: .3;
    float: right;
    margin-top: 19px;
    transform: rotate(-180deg);
}
</style>
