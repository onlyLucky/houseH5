<template>
	<view class="item">
		<view class="left-item" @tap="goDetail">
			<h1>党校房屋门面</h1>
			<view class="item-msg">
				<text>实际位置：党校支路8号附4号</text>
				<text>租约结束：2020.07.13</text>
				<text>下期收租日：2020.07.13</text>
			</view>
		</view>
		<view class="right-item">
			<image src="/static/icon/icon_return.png" lazy-load></image>
			<text class="status1">已收款</text>
		</view>
	</view>
</template>

<script>
	export default {
		methods:{
			goDetail () {
				uni.navigateTo({
					url:"/pages/index-detail/index-detail"
				})
			}
		}
	}
</script>

<style lang="less" scoped>
	.item{
		width: 100%;
		height: 250rpx;
		background-color: #FFFFFF;
		margin-top: 20rpx;
		padding: 39rpx 29rpx;
		box-sizing: border-box;
		display: flex;
		align-items: center;
		justify-content: space-between;
		.left-item{
			h1{
				font-size:30rpx;
				color: #000000;
			}
			.item-msg{
				margin-top: 20rpx;
				color: #969799;
				font-size: 26rpx;
				text{
					display: block;
					margin-bottom: 10rpx;
				}
			}
		}
		.right-item{
			display: flex;
			flex-direction: column;
			align-items: flex-end;
			image{
				width: 15rpx;
				height: 25rpx;
				margin-bottom: 105rpx;
			}
			text{
				font-size: 26rpx;
			}
			.status1{
				color: #1588FD;
			}
			.status2{
				color: #FF4527;
			}
		}
	}
</style>
