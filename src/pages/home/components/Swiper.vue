<template>
	<div class="wrapper">
		<swiper :options="swiperOption">
	    <swiper-slide v-for="item of swiperList" :key="item.id">
	    	<img class="swiper-img" :src="item.imgUrl"></swiper-slide>
	    <div class="swiper-pagination"  slot="pagination"></div>
	  </swiper>
  </div>
</template>

<script>
	export default {
		name: 'HomeSwiper',
		data () {
			return {
				swiperOption:{
					pagination: '.swiper-pagination',
					loop: true,
					autoplay: 3000,
				},
				swiperList: [{
					id: '0001',
					imgUrl: 'http://img1.qunarzz.com/piao/fusion/1809/31/da037478f37cf202.jpg_750x200_a02cf862.jpg'
				},
				{
					id: '0002',
					imgUrl: 'http://img1.qunarzz.com/piao/fusion/1809/c6/2467595fffc3b302.jpg_750x200_cca13d51.jpg'
				},
				{
					id: '0003',
					imgUrl: 'http://img1.qunarzz.com/piao/fusion/1809/87/534cf2e0a71fff02.jpg_750x200_5c778719.jpg'
				},
				{
					id: '0004',
					imgUrl: 'http://img1.qunarzz.com/piao/fusion/1807/18/39d4f01bb73a2d02.jpg_750x200_d761ba69.jpg'
				},
				{
					id: '0005',
					imgUrl: 'http://img1.qunarzz.com/piao/fusion/1809/c6/2467595fffc3b302.jpg_750x200_cca13d51.jpg'
				}]
			}
		}
	}
</script>

<style lang="stylus" scoped>
	.wrapper >>> .swiper-pagination-bullet-active
			background: white
	.wrapper
		overflow: hidden
		width: 100%
		height: 0
		padding-bottom: 26.67%
		background:#fff
		.swiper-img
			width: 100%
</style>