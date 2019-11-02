<template>
    <ul class="list">
        <li class="item">A</li>
        <li class="item">A</li>
        <li class="item">A</li>
        <li class="item">A</li>
    </ul>
</template>

<script>
export default {
    name:'CityAlphabet'
}
</script>

<style lang="stylus"> 
@import '~style/varibles.styl'
 .list
    display:flex
    float:right
    flex-direction :column
    justify-content :center
    position :absolute
    top: 1.58rem
    bottom :0
    color:$bgColor
    text-align :left
    // width: .4rem
    .item
      line-height :.44rem
      text-align: left
</style>