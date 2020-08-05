<template>
	<view class="form">
		<view class="form-item">
			<span class="formItem-title">手机号</span>
			<input type="text" value="" placeholder="请输入租赁手机号"/>
		</view>
		<view class="form-item">
			<span class="formItem-title">验证码</span>
			<input type="text" value="" placeholder="请输入验证码"/>
			<span class="code">获取验证码</span>
		</view>
		<view class="login-btn" @tap="goLogin">
			登录
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				
			};
		},
		methods:{
			goLogin () {
				console.log('hello')
				wx.switchTab({
					url:"../index/index"
				})
			}
		}
	}
</script>

<style lang="less" scoped>
	.form{
		width: 100%;
		padding: 28rpx;
		font-size: 30rpx;
		box-sizing: border-box;
		.form-item{
			width: 100%;
			position: relative;
			margin-top: 50rpx;
			.formItem-title{
				position: absolute;
				left: 0rpx;
				top: 0rpx;
				font-weight:500;
			}
			input{
				border-bottom:1rpx solid #E5E5E5;
				padding-left: 150rpx;
				padding-bottom: 19rpx;
			}
			.code{
				position: absolute;
				right: 0rpx;
				top: 0rpx;
				color: #1588FD;
			}
		}
		.login-btn{
			width: 100%;
			height: 88rpx;
			background-color: #1588FD;
			border-radius: 4rpx;
			text-align: center;
			line-height: 88rpx;
			color: #FFFFFF;
			font-size: 34rpx;
			margin-top: 60rpx;
		}
	}
	
</style>
