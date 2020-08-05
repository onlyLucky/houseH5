<template>
	<view class="index">
		<view class="index-box">
			<index-item></index-item>
			<index-item></index-item>
			<index-item></index-item>
			<index-item></index-item>
			<index-item></index-item>
			<index-item></index-item>
			<index-item></index-item>
			<index-item></index-item>
		</view>
		<view class="tabarShad"></view>
	</view>
</template>

<script>
	import indexItem from "./componts/indexItem.vue"
	export default {
		components: {
			indexItem
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

<style scoped lang="less">
	.index{
		width: 100vw;
		height: 100vh;
		background-color: #F7F8FA;
		.index-box{
			padding-bottom: 100rpx;
		}
		.tabarShad{
			width: 100%;
			height: 90rpx;
			position: fixed;
			bottom: 0rpx;
			box-shadow:0rpx 0rpx 17rpx 1rpx rgba(0, 0, 0, 0.05);
		}
	}
</style>
