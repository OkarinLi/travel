<template>
	<div>
		<home-header></home-header>
		<home-swiper></home-swiper>
		<home-icons></home-icons>
		<home-position></home-position>
	</div>
</template>

<script>
	import HomeHeader from './components/Header'
	import HomeSwiper from './components/Swiper'
	import HomeIcons from './components/Icons'
	import HomePosition from './components/Position'

	export default {
		name: 'Home',
		components: {
			HomeHeader,
			HomeSwiper,
			HomeIcons,
			HomePosition,
		}
	}
</script>

<style>
	
</style>