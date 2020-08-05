<template>
	<view class="map-tetail">
		<map class="map-con"></map>
		<view class="fixed">
			<image src="/static/icon/icon-fixed.png" lazy-load></image>
		</view>
		<view class="adress">
			<view class="adress-txt">党校支路8号附4号</view>
			<image src="/static/detail/adress.png" lazy-load></image>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				
			}
		},
		methods: {
			
		}
	}
</script>

<style lang="less" scoped>
	.map-con{
		width: 100vw;
		height: 100vh;
	}
	.fixed{
		position: fixed;
		bottom: 300rpx;
		right: 30rpx;
		width: 80rpx;
		height: 80rpx;
		border-radius: 50%;
		background-color: #FFFFFF;
		box-shadow:0rpx 6rpx 17rpx 1rpx rgba(32,34,49,0.06);
		display: flex;
		justify-content: center;
		align-items: center;
		image{
			width: 46rpx;
			height: 46rpx;
		}
	}
	.adress{
		width: 750rpx;
		height: 160rpx;
		padding: 32rpx;
		box-sizing: border-box;
		font-size: 30rpx;
		position: fixed;
		background-color: #FFFFFF;
		display: flex;
		bottom: 0rpx;
		justify-content: space-between;
		image{
			width: 80rpx;
			height: 80rpx;
		}
	}
</style>
