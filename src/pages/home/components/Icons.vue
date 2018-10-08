<template>
	<div class="icons">
		<swiper :options="swiperOption">
			<swiper-slide v-for="(page,index) of pages" :key="index">
				<div class="icon" v-for="item of page" :key="item.id">
					<div class="icon-img">
						<img class="icon-img-content" :src="item.imgUrl">
					</div>
					<p class="icon-desc">{{item.desc}}</p>
				</div>
			</swiper-slide>
			<div class="swiper-pagination"  slot="pagination"></div>
		</swiper>
	</div>
</template>

<script>
	export default {
		name: 'HomeIcons',
		data () {
			return {
				swiperOption:{
					autoplay: false,
					pagination: '.swiper-pagination',
				},
				iconList: [{
					id: '0001',
					imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png',
					desc: '景点门票'
				},
				{
					id: '0002',
					imgUrl: 'http://img1.qunarzz.com/piao/fusion/1804/5a/13ceb38dcf262f02.png',
					desc: '一日游'
				},
				{
					id: '0003',
					imgUrl: 'http://img1.qunarzz.com/piao/fusion/1804/ff/fdf170ee89594b02.png',
					desc: '厦门必游'
				},
				{
					id: '0004',
					imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/97/02f5043b51b2102.png',
					desc: '鼓浪屿'
				},
				{
					id: '0005',
					imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/96/c70f1e85ae4a4f02.png',
					desc: '自然风光'
				},
				{
					id: '0006',
					imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/50/26ffa31b56646402.png',
					desc: '亲子游'
				},
				{
					id: '0007',
					imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/89/55083b0f1951f302.png',
					desc: '两江夜游'
				},
				{
					id: '0008',
					imgUrl: 'https://img1.qunarzz.com/piao/fusion/1803/20/831d62d2e1c7be02.png',
					desc: '打卡圣地'
				},
				{
					id: '0009',
					imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/ee/5114069893722102.png',
					desc: '厦门观音山'
				}]
			}
		},
		computed: {
			pages () {
				const pages = []
				this.iconList.forEach((item,index)=>{
					const page = Math.floor(index / 8)
					if (!pages[page]){
						pages[page] = []
					}
					pages[page].push(item)
				})
				return pages
			}
		}
	}
</script>

<style lang="stylus" scoped>
	@import '~styles/varibles.styl'
	@import '~styles/mixins.styl'
	.icons >>> .swiper-container
		height: 0
		padding-bottom: 50% 
	.icons >>> .swiper-pagination-bullets
		position:absolute
		top :3.5rem
	.icon
		position: relative
		overflow: hidden
		float: left
		width: 25%
		height:0
		padding-bottom: 23%
		.icon-img
			position: absolute
			top: .1rem
			left: 0
			right: 0
			bottom: .44rem
			height: 1.3rem
			box-sizing: border-box
			padding: .1rem
			.icon-img-content
				display: block
				margin: 0 auto
				height: 1.1rem
				width:1.1rem
		.icon-desc
			position: absolute
			left: 0
			right: 0
			bottom: 0
			top: 1.4rem
			height: .28rem
			line-height: .28rem
			color: $darkTextColor
			text-align: center
			ellipsis()
</style>