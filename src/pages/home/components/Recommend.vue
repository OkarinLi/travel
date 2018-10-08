<template>
	<div>
		<div class="space"></div>
		<div class="recommend-title">💕猜你喜欢</div>
		<ul>
			<li v-for="item of recommendList" :key="item.id" class="item border-bottom">
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
		data () {
			return {
				recommendList: [{
					id: '0001',
					imgUrl: 'http://img1.qunarzz.com/sight/p0/1805/7d/7dca9c37a87479eba3.img.jpg_200x200_f62f78bd.jpg',
					title: '世茂云上厦门观光厅',
					desc: '⭐️⭐️⭐️⭐️⭐️    2970条评论',
					district: '思明区'
				},
				{
					id: '0002',
					imgUrl: 'http://img1.qunarzz.com/sight/p0/1508/97/ea51af995c4d4de85c53855302b2f5af.water.jpg_200x200_ee569936.jpg',
					title: '鼓浪屿往返轮渡',
					desc: '⭐️⭐️⭐️⭐️⭐️    25165条评论',
					district: '鼓浪屿'
				},
				{
					id: '0003',
					imgUrl: 'http://img1.qunarzz.com/sight/p0/1711/fe/fe517fa5a183e4bca3.img.jpg_200x200_1afe21c0.jpg',
					title: '厦门老院子景区',
					desc: '⭐️⭐️⭐️⭐️⭐️    1350条评论',
					district: '集美区'
				},
				{
					id: '0004',
					imgUrl: 'http://img1.qunarzz.com/sight/p0/1506/f6/f6b727f036fe5d6d.water.jpg_200x200_a3c26b4d.jpg',
					title: '鼓浪屿',
					desc: '⭐️⭐️⭐️⭐️⭐️    38908条评论',
					district: '思明区'
				},
								{
					id: '0005',
					imgUrl: 'http://img1.qunarzz.com/sight/p0/1708/5b/5b037e5c218a1d2aa3.img.jpg_200x200_4fb3e98d.jpg',
					title: '厦门海底世界',
					desc: '⭐️⭐️⭐️⭐️⭐️    6157条评论',
					district: '鼓浪屿'
				},
								{
					id: '0006',
					imgUrl: 'http://img1.qunarzz.com/sight/p0/1706/e5/e563e6454d1771c2a3.img.jpg_200x200_9c5b5a22.jpg',
					title: '厦门方特梦幻王国',
					desc: '⭐️⭐️⭐️⭐️⭐️    8696条评论',
					district: '集美区'
				},
				{
					id: '0007',
					imgUrl: 'http://img1.qunarzz.com/sight/p0/1804/53/530392bdcdbf917ba3.img.jpg_200x200_f5b2c3f4.jpg',
					title: '厦门科技馆',
					desc: '⭐️⭐️⭐️⭐️⭐️    5442条评论',
					district: '思明区'
				}
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