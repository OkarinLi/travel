<template>
	<div>
		<div class="recommend-title">周末去哪儿</div>
		<div v-for="item of recommendList" :key="item.id" class="item item border-bottom">
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
		data () {
			return {
				recommendList: [{
					id: '0001',
					imgUrl: 'http://img1.qunarzz.com/sight/source/1711/15/1cdd5ee885686b.jpg_r_640x214_46768064.jpg',
					title: '厦门必游TOP10',
					desc: '来厦门感受一把小资情调',
				},
				{
					id: '0002',
					imgUrl: 'http://img1.qunarzz.com/sight/source/1511/8f/bf3a40e4afcf29.jpg_r_640x214_90225212.jpg',
					title: '泉心泉意',
					desc: '这个秋冬不干燥，养生休闲一举两得',
				},
				{
					id: '0003',
					imgUrl: 'http://img1.qunarzz.com/sight/source/1505/b3/671f666cc7845a.jpg_r_640x214_f977f30c.jpg',
					title: '帆船游艇出海',
					desc: '乘风破浪，直挂云帆济沧海',
				},
				{
					id: '0004',
					imgUrl: 'http://img1.qunarzz.com/sight/source/1505/ae/15c0516f565a02.jpg_r_640x214_b8176bc2.jpg',
					title: '签到鼓浪屿',
					desc: '在鼓浪屿那些你不可错过的风景',
				},
								{
					id: '0005',
					imgUrl: 'http://img1.qunarzz.com/sight/source/1606/53/c5ebb7bf59681b.jpg_r_640x214_8cf5e397.jpg',
					title: '游轮观光之旅',
					desc: '乘坐游轮爱上厦门的高大上',
				},
				]
			}
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