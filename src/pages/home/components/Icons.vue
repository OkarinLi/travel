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
		props: {
			list: Array
		},
		data () {
			return {
				swiperOption:{
					autoplay: false,
					pagination: '.swiper-pagination',
				},
			}
		},
		computed: {
			pages () {
				const pages = []
				this.list.forEach((item,index)=>{
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