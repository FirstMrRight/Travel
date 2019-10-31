<template>
	<div>
	<HomeHeader :city="city"></HomeHeader>
	<home-swiper :list="swiperList"></home-swiper>
	<home-icons :list="iconList"></home-icons>
	<home-recommend :list="recommendList"></home-recommend>
	<home-weekends :list="weekendList"></home-weekends>
</div>
</template>
<script>
	import HomeHeader from './components/Header'
	import HomeSwiper from './components/Swiper'
	import HomeIcons from './components/Icons'
	import HomeRecommend from './components/Recommend'
	import HomeWeekend from './components/Weekend'
	import HomeWeekends from './components/Weekends'
	import axios from 'axios'
	export default {
		name: 'Home',
		components: {
			HomeHeader,
			HomeSwiper,
			HomeIcons,
			HomeRecommend,
			HomeWeekend,
			HomeWeekends
		},
		data () {
			return {
				city: '',
				swiperList:[],
				iconList:[],
				recommendList:[],
				weekendList:[]
			}
		},
		methods :{
			getHomeInfo () {
				axios.get('/api/index.json')
					.then(this.getHomeInfoSucc)
			},
			getHomeInfoSucc(res) {
				//从服务端获取的全部数据，注意数据结构
				console.log(res)
				res=res.data;
				if (res.ret && res.data){
					const data =res.data;
					this.city= data.city;
					console.log(this.city);
					this.swiperList=data.swiperList;
					console.log(this.swiperList)
					this.iconList=data.iconList;
					console.log(this.iconList)
					this.recommendList=data.recommendList;
					console.log(this.recommendList);
					this.weekendList=data.weekendList;
					console.log(this.weekendList)
				}
			}
		},
		mounted () {
			this.getHomeInfo();
		}
	}
</script>