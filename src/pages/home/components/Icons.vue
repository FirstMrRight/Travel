<template>
  <div class="icons">
        <div
          class="icon"
          v-for="item of iconList"
          :key="item.id"
        >
          <div class='icon-img'>
            <img class='icon-img-content' :src='item.imgUrl' />
          </div>
          <p class="icon-desc">{{item.desc}}</p>
        </div>
  </div>
</template>

<script>
export default {
  name: 'HomeIcons',
  props: {
    list: Array
  },
   data () {
        return {
            iconList:[{
                id: '0001',
                imgUrl: 'https://imgs.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png',
                desc:'景点门票'
            },{
                id: '0002',
                imgUrl: 'https://imgs.qunarzz.com/piao/fusion/1804/5a/13ceb38dcf262f02.png',
                desc:'一日游'
            },{
                id: '0003',
                imgUrl: 'https://imgs.qunarzz.com/piao/fusion/1804/ff/fdf170ee89594b02.png',
                desc:'青岛必游'
            },{
                id: '0004',
                imgUrl: 'https://imgs.qunarzz.com/piao/fusion/1803/89/55083b0f1951f302.png',
                desc:'帆船体验'
            },{
                id: '0005',
                imgUrl: 'https://imgs.qunarzz.com/piao/fusion/1803/50/26ffa31b56646402.png',
                desc:'青岛海底世界'
            },{
                id: '0006',
                imgUrl: 'https://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20194/f04285731d7121da1b9028e2bf431695.png',
                desc:'崂山'
            },{
                id: '0007',
                imgUrl: 'https://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20194/8671dfb53aecb10748c86b4c29971a14.png',
                desc:'青岛动物园'
            },{
                id: '0008',
                imgUrl: 'https://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20194/e48e868a92b508a04da2a3bfdd35d4cd.png',
                desc:'青啤博物馆'
            // },{
            //     id: '0009',
            //     imgUrl: 'https://imgs.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png',
            //     desc:'青岛极地'
            // },
            },]

            }
    },
  /*
  * 计算属性：根据数据项的不同，去计算
  * 使用其功能，计算第一页显示什么，第二页显示什么
  * */
  // computed: {
  //   pages () {
  //     const pages = []
  //     this.iconList.forEach((item, index) => {
  //       /*
  //       * floor:取整
  //       * */
  //       const page = Math.floor(index / 8)
  //       if (!pages[page]) {
  //         pages[page] = []
  //       }
  //       pages[page].push(item)
  //     })
  //     return pages
  //   }
  // }
}
</script>

<style lang="stylus" scoped>
  @import '~style/varibles.styl'
  @import '~style/mixins.styl'
   
  .icons
    height: 0
    padding-bottom: 50%
    margin-top: .1rem
    .icon
      position: relative
      overflow: hidden
      float: left
      width: 25%
      height: 0
      padding-bottom: 25%
      .icon-img
        position: absolute
        top: 0
        left: 0
        right: 0
        bottom: .44rem
        box-sizing: border-box
        padding: .1rem
        .icon-img-content
          display: block
          margin: 0 auto
          height: 100%
      .icon-desc
        position: absolute
        left: 0
        right: 0
        bottom: 0
        height: .44rem
        line-height: .44rem
        text-align: center
        color: $darkTextColor
        ellipsis()
</style>
