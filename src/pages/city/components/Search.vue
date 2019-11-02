<template>
    <div>
        <div class="search">
            <input class="search-input" type="text" placeholder="请输入城市名字或拼音">
        </div>
    </div>
</template>

<script>
export default {
    name:'CitySearch'
}
</script>

<style lang='stylus' scoped>
    @import '~style/varibles.styl'
    .search
      height .72rem
      background :$bgColor
      padding 0 .1rem
      .search-input
        width:100%
        height : .62rem
        padding:0 .1rem
        line-height: .62rem
        text-align :center
        border radius .06rem
        color:#666
</style>