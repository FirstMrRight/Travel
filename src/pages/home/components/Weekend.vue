<template>
<div>

    <div class="title">周末去哪</div>
     <ul>
        <li class="item border-bottom" v-for="item of recommendList" :key="item.id">
            <div class="item-img-wrapper">
                <img class="item-img" :src="item.imgUrl"/>
            </div>
            <div class="item-info">
                <p class="item-title">{{item.title}}</p>
                <p class="item-desc">{{item.desc}}</p>
            </div>
        </li>
     </ul>
</div>
</template>

<script>
export default {
    name: 'HomeWeeked',
    props: {
        // list:Array
    },
    data () {
        return {
            recommendList:[{
                id: '0001',
                imgUrl: 'https://imgs.qunarzz.com/sight/source/1505/85/708da4ab8dba17.jpg_r_640x214_d3d8cfa5.jpg',
                title:'大连圣亚海洋世界',
                desc:'浪漫大连首站，浪漫海洋主题乐园'
            },{
                id: '0002',
                imgUrl: 'https://imgs.qunarzz.com/sight/source/1509/fb/8a282060176455.jpg_r_640x214_eee8f443.jpg',
                title:'畅游云南世界',
                desc:'洱海吉普游艇+玉龙雪山拉市海+喂红嘴鸥'
            },{
                id: '0003',
                imgUrl: 'https://imgs.qunarzz.com/sight/source/1505/94/f48c88a43966be.jpg_r_640x214_629e5387.jpg',
                title:'杭州西湖',
                desc:'苏州园林3日2晚游 天堂苏杭 精致旅行'
            },]
        }
    }
}
</script>

<style lang="stylus" scoped>
    @import '~style/mixins.styl';
    .title
      line-height: .4rem
      background :#eee
      margin-top : .2rem
      text-indent: .2rem
    .item-img-wrapper
      width: 100%
      height :1.7rem
      padding-bottom: 15%
      .item-img
        width: 100%
    .item-info
      flex:1
      padding: .1rem
    .item-title
      line-height: .54rem
      font-size: .32rem
      ellipsis()
    .item-desc
      line-height: .4rem
      color:#ccc
      ellipsis()    
</style>