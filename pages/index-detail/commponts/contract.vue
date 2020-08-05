<template>
	<view class="contract">
		<view class="upfile">
			<image src="/static/detail/pdf@2x.png" lazy-load></image>
		</view>
		<view class="downBtn">下载合同</view>
	</view>
</template>

<script>
</script>

<style lang="less" scoped>
	.contract{
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		margin-top: 60rpx;
		.upfile{
			width:461rpx;
			height:276rpx;
			background:rgba(225,226,230,1);
			border-radius:10rpx;
			display: flex;
			justify-content: center;
			align-items: center;
			image{
				width: 100rpx;
				height: 100rpx;
			}
		}
		.downBtn{
			margin-top: 60rpx;
			width:280rpx;
			height:88rpx;
			background:#FFFFFF;
			border:1rpx solid #1588FD;
			border-radius:4rpx;
			color: #1588FD;
			text-align: center;
			line-height: 88rpx;
			font-size: 32rpx;
		}
	}
</style>
