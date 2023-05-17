<template>
	<view class="banner-box">
		<view class="banner-bg" :style="{'backgroundImage': `linear-gradient(${bannerBackground || '#009B8C'} 50%, #FFF)`}"></view>
		<swiper class="banner-swiper"
			indicator-dots
			indicator-color="rgba(255,255,255,0.5)"
			indicator-active-color="#FFF"
			:interval="4000"
			autoplay
			circular
			:current="current"
			@change="handleSwiperChange"
			>
			<!-- previous-margin="15" next-margin="15" circular -->
			<swiper-item class="swiper-item" v-for="(item, index) in bannerList" :key="index">
				<image :src="item.imageUrl"></image>
			</swiper-item>
		</swiper>
	</view>
</template>

<script>
	export default {
		props: {
			bannerList: {
				type: Array,
				default: () => [
				{
					id: 1,
					imageUrl: '/static/images/it01.png',
					background: '#009B8C',
					advertUrl: '/pages/course/course-details'
				},
				{
					id: 2,
					imageUrl: '/static/images/it02.png',
					background: '#6E3DE6',
					advertUrl: '/pages/course/course-details'
				},
				{
					id: 3,
					imageUrl: '/static/images/it03.png',
					background: '#0D81ED',
					advertUrl: '/pages/course/course-details'
				},
				{
					id: 4,
					imageUrl: '/static/images/it04.png',
					background: '#009700',
					advertUrl: '/pages/course/course-details'
				},
				]
			}
		},
		data() {
			return {
				current: 0, //当前所在滑块的 index
				bannerBackground: '#009B8C' // 背景色
			}
		},
		methods: {
			handleSwiperChange(e) {
				this.bannerBackground = this.bannerList[e.detail.current].background;
			}
		}
	}
</script>

<style lang="scss">
	.banner-box {
		padding-top: 120rpx;

		/* #ifdef APP-PLUS */
		// padding-top: calc(var(--status-bar-height) + 80rpx);
		/* #endif */
		position: relative;

		.banner-bg {
			position: absolute;
			top: 0rpx;
			width: 100%;
			height: 470rpx;
			transform: .5s;
		}

		.banner-swiper {
			width: 100%;
			height: 350rpx;

			.swiper-item {
				width: 100%;
				height: 100%;
				padding: 0 30rpx;
				box-sizing: border-box;
				
				image {
					width: 100%;
					height: 100%;
					border-radius: 15rpx;
				}
			}
		}
	}
</style>