<template>
	<view class="check-info">
		<view class="info">
			<view class="info-item-up">
				<view class="info-title">承租人</view>
				<view class="info-txt">马冬梅</view>
			</view>
			<view class="info-item-up">
				<view class="info-title">身份证</view>
				<view class="info-txt">45674567567856</view>
			</view>
			<view class="info-item-up">
				<view class="info-title">租约状态</view>
				<view class="info-txt">租赁中</view>
			</view>
			<view class="info-item-up">
				<view class="info-title">租约起止</view>
				<view class="info-txt">2020.07.13 — 2020.08.19</view>
			</view>
			<view class="info-item-up">
				<view class="info-title">房屋租金</view>
				<view class="info-txt">2000（元）</view>
			</view>
			<view class="info-item-up">
				<view class="info-title">房屋租金</view>
				<view class="info-txt">2000（元）</view>
			</view>
			<view class="info-item-up">
				<view class="info-title">开始收租</view>
				<view class="info-txt">2020.07.13</view>
			</view>
			<view class="info-item-up">
				<view class="info-title">房屋租金</view>
				<view class="info-txt">2000（元）</view>
			</view>
			<view class="info-item-up">
				<view class="info-title">下期收租日</view>
				<view class="info-txt">2020.08.14</view>
			</view>
			<view class="line"></view>
			<view class="info-item-down">
				<view class="info-title">资产名称</view>
				<view class="info-txt">党校房屋门面</view>
			</view>
			<view class="info-item-down">
				<view class="info-title">产权单位</view>
				<view class="info-txt">南州投资</view>
			</view>
			<view class="info-item-down">
				<view class="info-title">坐落位置</view>
				<view class="info-txt">党校支路8号附4号</view>
			</view>
			<view class="info-item-down">
				<view class="info-title">实际位置</view>
				<view class="info-txt">党校支路8号附4号</view>
			</view>
			<view class="info-item-down">
				<view class="info-title">资产用途</view>
				<view class="info-txt">办公楼</view>
			</view>
		</view>
		<view class="map">
			<view class="map-header" @tap="goMapDetail">
				<h1 class="header-left">导航指引</h1>
				<image src="/static/icon/icon_return.png" lazy-load></image>
			</view>
			<map class="map-content"></map>
			<div class="backHouseBtn" @tap="goBackHouse">
				我要退租
			</div>
			<!-- <div class="backHouseBtn">
				查看退租进度
			</div> -->
		</view>
	</view>
</template>

<script>
	export default {
		methods:{
			goBackHouse () {
				uni.navigateTo({
					url: "/pages/back-reason/back-reason"
				})
			},
			goMapDetail () {
				uni.navigateTo({
					url: "/pages/map-to/map-to"
				})
			}
		}
	}
</script>

<style lang="less" scoped>
	.check-info{
		width: 100vw;
		padding: 20rpx 30rpx;
		position: relative;
		box-sizing: border-box;
		.info{
			width: 100%;
			padding: 40rpx 30rpx;
			box-sizing: border-box;
			border-radius:10rpx;
			background-color: #FFFFFF;
			font-size: 28rpx;
			.info-item-up{
				display: flex;
				margin-bottom: 27rpx;
			}
			.info-item-down{
				display: flex;
				margin-top: 27rpx;
			}
			.info-title{
				width: 170rpx;
				display: block;
				text-align: left;
				color: #999999;
			}
			.info-txt{
				width: 460rpx;
				color: #000000;
			}
			.line{
				width: 100%;
				height: 1px;
				background-color: #E6E6E6;
			}
		}
		.map{
			height: 660rpx;
			position: relative;
			.map-header{
				width: 100%;
				height: 86rpx;
				display: flex;
				justify-content: space-between;
				align-items: center;
				h1{
					font-size:28rpx;
					font-weight:400;
					color: #000000;
				}
				image{
					width:15rpx;
					height:26rpx;
				}
			}
			.map-content{
				width: 100%;
				height: 240rpx;
				background-color: gray;
			}
			.backHouseBtn{
				display: block;
				position: absolute;
				top: 370rpx;
				width: 691rpx;
				height: 88rpx;
				background-color: #FFFFFF;
				border:1rpx solid #1588FD;
				border-radius:4rpx;
				text-align: center;
				line-height: 88rpx;
				font-size: 30rpx;
				color: #1588FD;
			}
		}
	}
</style>
