<template>
	<div>
		<div class="recommend-title">周末去哪儿</div>
		<div v-for="item of list" :key="item.id" class="item border-bottom">
			<img class="item-img" :src="item.imgUrl">
			<div class="item-info">
				<p class="item-title">{{item.title}}</p>
				<p class="item-desc">{{item.desc}}</p>
			</div>
		</div>

	</div>
</template>

<script>
	export default{
		name: 'HomeWeekend',
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
		background: #eee
	.item
		height: 4.1rem
		.item-img
			width: 7.5rem
			height: 2.8rem
		.item-info
			flex: 1
			padding: .1rem
			min-width: 0
			padding: .1rem
			.item-title
				text-indent: .1rem
				line-height: .54rem
				font-size: .28rem
				ellipsis()
			.item-desc
				text-indent: .1rem
				line-height: .4rem
				font-size: .24rem
				color: #5b5b5b
				ellipsis()
</style>