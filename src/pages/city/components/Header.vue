<template>
    <div class="header">
        城市选择
        <!-- 页面跳转到根目录下 -->
        <router-link to="/" class="header-back">
            <div class="iconfont header-back">&#xe624;</div>
        </router-link>
    </div>
</template>

<script>
export default {
    name: 'CityHeader'
}
</script>

<style lang="stylus" scoped>
    @import '~style/varibles.styl'
    .header
      overflow:hidden
      line-height :$headerHeight
      text-align: center
      color:#fff
      background :$bgColor
      font size .32rem
      .header-back
        // padding-left:.1rem
        position :absolute
        top:0
        width :.64rem
        left:0
        text-align :center
        font size .4rem
        color:#fff
</style>