<template>
	<div class="position">
		<ul class="position-ul">
			<li class="position-li border">
				<span class="iconfont">&#xe652;</span>
				定位失败
			</li>
			<li class="position-li border-top">
				<span class="iconfont">&#xe654;</span>
				玩水季
			</li>
		</ul>
<!-- 		<div class="position-content">
			<span class="iconfont">&#xe652;</span>
			定位失败
		</div>
		<div class="position-content">
			<span class="iconfont">&#xe654;</span>
			玩水季
		</div> -->
	</div>
</template>

<script>
	export default {
		name: 'HomePosition'
	}
</script>

<style lang="stylus" scoped="">
	.position
		height: 1rem
		width: 100%
		.position-ul
			text-align: center
			.position-li
				box-sizing: border-box
				width:50%
				float: left
				line-height: 1rem
				// border-top: 1px solid #e8e8e8
			// .left
			// 	border-right: 1px solid #e8e8e8
	
</style>