<template>
  <div id="app">
    <vheader></vheader>
    <ul class="tab">
        <li class="tab-item">
          <router-link to="/goods">商品</router-link>
        </li>
        <li class="tab-item">
          <router-link to="/ratings">评价</router-link>
        </li>
        <li class="tab-item">
          <router-link to="/seller">商家</router-link>
        </li>
    </ul>
    <router-view/>
  </div>
</template>

<script>
  import vheader from './components/header/header.vue'
export default {
  name: 'App',

  components: {
    vheader: vheader
  }
}
</script>

<style lang="stylus" rel="stylesheet/stylus" scoped>
.tab
  height: 40px
  display: flex
  border-bottom: 1px solid rgba(7, 17, 27, 0.1)
  .tab-item
    flex: 1
    text-align: center
    line-height: 40px
    font-size: 14px
    color: rgb(77, 85, 93)
    .router-link-active
      font-size: 14px
      color: rgb(240, 20, 20)
</style>
