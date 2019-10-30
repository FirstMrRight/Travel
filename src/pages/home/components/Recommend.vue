<template>
<div>

    <div class="title">热销推荐</div>
     <ul>
        <li class="item border-bottom" v-for="item of recommendList" :key="item.id">
            <div class="item-img-wrapper">
                <img class="item-img" :src="item.imgUrl"/>
            </div>
            <div class="item-info">
                <p class="item-title">{{item.title}}</p>
                <p class="item-desc">{{item.desc}}</p>
                <button class="item-button">查看详情</button>
            </div>
        </li>
     </ul>
</div>
</template>

<script>
export default {
    name: 'HomeRecommend',
    props: {
        // list:Array
    },
    data () {
        return {
            recommendList:[{
                id: '0001',
                imgUrl: 'https://imgs.qunarzz.com/p/p19/1809/b9/2a3d362aabcbb02.jpg_256x160_28907832.jpg',
                title:'大连圣亚海洋世界',
                desc:'浪漫大连首站，浪漫海洋主题乐园'
            },{
                id: '0002',
                imgUrl: 'https://imgs.qunarzz.com/vs_ceph_vs_tts/0385018d-04a5-405c-a583-23da4451458d.jpg_r_480x320x90_c280b5b9.jpg',
                title:'畅游云南世界',
                desc:'洱海吉普游艇+玉龙雪山拉市海+喂红嘴鸥'
            },{
                id: '0003',
                imgUrl: 'https://imgs.qunarzz.com/p/p70/1809/e7/4941057a6aae702.jpg_256x160_9fee6ccb.jpg',
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
    .item
      display: flex  //弹性布局
      height : 1.9rem
      .item-img
        width: 1.7rem
        height :1.7rem
        padding: .2rem
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
        .item-button
          line-height : .44rem
          margin-top .16rem
          background: #ff9300
          padding: 0 .2rem
          border-radius: .06rem
          color: #fff
          
</style>