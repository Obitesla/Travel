<template>
  <div>
    <div class="header">
      <div class="header-left">
        <div class="iconfont back-icon">&#xe6a3;</div>
      </div>
      <div class="header-input">
        <span class="iconfont">&#xe6a2;</span>
        输入城市/景点/游玩主题
      </div>
      <router-link to="/city">
        <div class="header-right">
          {{this.city}}
          <span class="iconfont arrow-icon">&#xe66c;</span>
        </div>
      </router-link>
    </div>
  </div>
</template>

<script>
import {mapState} from 'vuex'
export default {
  name: 'HomeHeader',
  computed: {
    ...mapState(['city'])
  }
}
</script>

<style lang="stylus" scoped>
  @import '~styles/varibles.styl'
  .header
    display:flex
    line-height: $headerHeight
    background $bgColor //dbColor为所设置的全局的一个背景色，在‘@/assets/styles/varibles.styl’中更改
    color #ffffff
    .header-left
      width .64rem
      float: left
      .back-icon
        text-align center
        font-size .4rem
    .header-input
      flex: 1
      padding-left .2rem
      background #ffffff
      height .64rem
      line-height .64rem
      margin-top .12rem
      margin-left .2rem
      border-radius .1rem
      color: #ccc
    .header-right
      min-width: 1.04rem
      padding 0 .1rem
      float: right
      text-align center
      color #ffffff
      .arrow-icon
        margin-left -0.04rem
        font-size .24rem
</style>
