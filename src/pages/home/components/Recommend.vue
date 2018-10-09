<template>
	<div>
		<div class="space"></div>
		<div class="recommend-title">💕猜你喜欢</div>
		<ul>
			<li v-for="item of list" :key="item.id" class="item border-bottom">
				<img class="item-img" :src="item.imgUrl">
				<div class="item-info">
					<p class="item-title">{{item.title}}</p>
					<p class="item-desc">{{item.desc}}</p>
					<p class="item-district">{{item.district}}</p>
				</div>
			</li>
		</ul>
	</div>
</template>

<script>
	export default{
		name: 'HomeRecommend',
		props: {
			list: Array
		}
	}
</script>

<style lang="stylus" scoped>
	@import '~styles/mixins.styl'
	.recommend-title
		line-height: .8rem
		text-indent: .2rem
		font-size: .32rem
	.space
		background: #eee
		height: .2rem
	.item
		display: flex
		height: 2.4rem
		.item-img
			width: 2rem
			height: 2rem
			padding: .2rem
		.item-info
			flex: 1
			padding: .1rem
			min-width: 0
			.item-title
				line-height: .54rem
				font-size: .34rem
				padding-top: .4rem
				ellipsis()
			.item-desc
				line-height: .4rem
				font-size: .24rem
				color: #5b5b5b
				margin-top: .1rem
				margin-left: .1rem
				ellipsis()
			.item-district
				font-size: .24rem
				color: #5b5b5b
				float: right
				margin-top: .2rem
				margin-right: .5rem	
</style>