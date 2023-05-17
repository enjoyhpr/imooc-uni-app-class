<template>
	<view class="index-box">
		<!-- 搜索组件 -->
		<!-- #ifdef MP -->
		<search-input></search-input>
		<!-- #endif -->
		<!-- 轮播图组件 -->
		<my-banner></my-banner>
		<!-- 分类组件 -->
		<category-box></category-box>
		<!-- 课程滑块 -->
		<swiper-course></swiper-course>
	</view>
</template>

<script>
	import searchInput from '@/components/common/search-input.vue'
	import myBanner from '@/components/common/my-banner.vue'
	import categoryBox from './components/category-box.vue'
	import swiperCourse from './components/swiper-course.vue'
	export default {
		components: {
			searchInput,
			myBanner,
			categoryBox,
			swiperCourse
		},
		data() {
			return {
				title: 'Hello'
			}
		},
		onLoad() {

		},
		methods: {

		}
	}
</script>

<style>
	.content {
		display: flex;
		flex-direction: column;
		align-items: center;
		justify-content: center;
	}

	.logo {
		height: 200rpx;
		width: 200rpx;
		margin-top: 200rpx;
		margin-left: auto;
		margin-right: auto;
		margin-bottom: 50rpx;
	}

	.text-area {
		display: flex;
		justify-content: center;
	}

	.title {
		font-size: 36rpx;
		color: #8f8f94;
	}

	.orange {
		color: orange;
	}
</style>