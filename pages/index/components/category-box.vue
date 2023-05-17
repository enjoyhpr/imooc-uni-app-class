<template>
	<view class="category-box">
		<view v-for="(item, index) in categoryList.slice(0, 7)" :key="index">
			{{item.name}}
		</view>
		<view>全部分类</view>
	</view>
</template>

<script>
	export default {
		props: {
			categoryList: {
				type: Array,
				default: () => [{
						id: 1,
						name: 'java'
					},
					{
						id: 2,
						name: '运维'
					},
					{
						id: 3,
						name: 'Python'
					},
					{
						id: 4,
						name: 'UI设计'
					},
					{
						id: 5,
						name: '大数据'
					},
					{
						id: 6,
						name: '前端'
					},
					{
						id: 7,
						name: 'PHP'
					},
					{
						id: 8,
						name: 'Vue'
					},
				]
			},
		}
	}
</script>

<style lang="scss">
	.category-box {
		display: flex;
		flex-wrap: wrap;
		justify-content: space-around;
		padding: 20rpx 30rpx 0 30rpx;
		
		>view {
			width: 160rpx;
			height: 70rpx;
			background: #F8F9FB;
			text-align: center;
			line-height: 70rpx;
			font-size: 26rpx;
			border-radius: 20rpx;
			margin-top: 15rpx;
		}
	}
</style>