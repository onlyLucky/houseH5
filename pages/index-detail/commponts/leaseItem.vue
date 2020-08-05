<template>
	<view class="item">
		<view class="item-title">账期：2020.07.13-2020.08.12</view>
		<view class="item-content-pass">
			<view class="con-tit">
				<view class="tit-left">房屋押金</view>
				<view class="tit-right status1">已支付</view>
			</view>
			<view class="con-all" v-show="true">
				<view class="txt-up">账单金额：¥2000</view>
				<view class="txt-up">应收款日：2020.07.13</view>
				<view class="line"></view>
				<view class="txt-down">已收款：¥2000</view>
				<view class="txt-down">收款日期：2020.07.13</view>
			</view>
			<view class="con-part" v-show="false">
				<view class="part-left">
					<view class="txt-up">账单金额：¥2000</view>
					<view class="txt-up">应收款日：2020.07.13</view>
				</view>
				<view class="part-right">立即支付</view>
			</view>
		</view>
	</view>
</template>

<script>
</script>

<style lang="less" scoped>
	.item{
		margin-top: 20rpx;
		.item-title{
			color: #969799;
			font-size: 24rpx;
			margin-left: 30rpx;
			padding: 15rpx 0;
		}
		.item-content-pass{
			width: 750rpx;
			padding: 40rpx 30rpx;
			box-sizing: border-box;
			background-color: #FFFFFF;
		}
		.con-tit{
			display: flex;
			justify-content: space-between;
			color: #000000;
			font-size: 30rpx;
		}
		.con-all{
			color: #969799;
			font-size: 26rpx;
			margin-top: 10rpx;
			.txt-up{
				margin-bottom: 10rpx;
			}
			.line{
				width: 100%;
				height: 1rpx;
				background-color: #DCDDE0;
			}
			.txt-down{
				margin-top: 10rpx;
			}
		}
		.con-part{
			margin-top: 10rpx;
			color: #969799;
			font-size: 26rpx;
			display: flex;
			justify-content: space-between;
			align-items: center;
			.txt-up{
				margin-top: 10rpx;
			}
			.part-right{
				width:140rpx;
				height:56rpx;
				border:1rpx solid #1588FD;
				border-radius:6rpx;
				text-align: center;
				line-height: 56rpx;
				color: #1588FD;
			}
		}
		.status1{
			color: #54C772;
		}
		.status2{
			color: #FF211C;
		}
		.status3{
			color: #979899;
		}
	}
</style>
