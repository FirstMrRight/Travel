<template>
    <div class="wrapper">
        <swiper :options="swiperOption">
                <swiper-slide v-for="item of list" :key="item.id">
                <img class="swiper-img" :src="item.imgUrl"/>
            </swiper-slide>
             <div class="swiper-pagination"  slot="pagination"></div>
        </swiper>  
    </div>
</template>

<script>
export default {
  name: 'HomeSwiper',
props:{
  list:Array
},
  data () {
    return {
      swiperOption: {
        pagination: '.swiper-pagination',
        loop:true,
        list:Array
      },
      // swiperList: [{
      //     id: '0001',
      //     imgUrl:'https://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/201910/fcc952d6b479db0e7e61922f3ee70f04.jpg_750x200_c5b67f70.jpg'
      // },{
      //     id: '0002',
      //     imgUrl:'https://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/201910/0ee1d3f10d0caea8fd988a049f4f4664.jpg_750x200_51e898d3.jpg'
      // },{
      //     id: '0003',
      //     imgUrl:'https://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/201910/78b240572657a6da67e662540c846dd6.jpg_750x200_b75c8be9.jpg'
      // }
      // ]
    }
  },
  computed: {
    showSwiper () {
      return this.list.length
      auto:false
    }
  }
}
</script>

<style lang="stylus" scoped>
    .wrapper >>> .swiper-pagination-bullet-active
      background : #eee
    .wrapper
      overflow hidden
      width :100%
      height :0
      padding-bottom :27.25%
      background :#eee
      .swiper-img
        width: 100%

</style>