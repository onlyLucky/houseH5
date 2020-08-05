<template>
	<view class="reason">
		<view class="reason-box">
			<radio-group @change="radioChange">
				<label class="radio-box" v-for="(item, index) in selectList" :key="item.value">
					<view class="radio-btn">
						<radio :value="item.value" :checked="index === current" />
					</view>
					<view class="radio-txt">{{item.name}}</view>
				</label>
			</radio-group>
			<view class="line"></view>
			<textarea class="textarea" placeholder="输入内容" :maxlength="100" placeholder-style="font-size:28rpx"/>
		</view>
		<view class="submitBtn">提交</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				current: 0,
				selectList:[
					{
						value:'1',
						name: '合同到期退租',
						checked: 'true'
					},
					{
						value:'2',
						name: '工作、生活地点调动'
					},
					{
						value:'3',
						name: '社区硬件配套不满意'
					},
					{
						value:'4',
						name: '工经营问题退租'
					},
					{
						value:'5',
						name: '其它原因'
					}
				]
			}
		},
		methods: {
			
		}
	}
</script>

<style lang="less" scoped>
	.reason{
		width: 100vw;
		height: 100vh;
		background-color: #F5F6FA;
		padding: 20rpx 30rpx;
		box-sizing: border-box;
		.reason-box{
			width: 100%;
			height: 600rpx;
			border-radius:10rpx;
			background-color: #FFFFFF;
			box-sizing: border-box;
			padding: 30rpx;
		}
		.radio-box{
			display: flex;
			align-items: center;
			margin-bottom: 30rpx;
			justify-content: flex-start;
			.radio-btn{
				margin-right: 30rpx;
			}
			.radio-txt{
				line-height: 44rpx;
				font-size: 28rpx;
			}
		}
		.line{
			width: 100%;
			height: 1rpx;
			background-color: #D7D8DB;
			margin-bottom: 30rpx;
		}
		.textarea{
			font-size: 28rpx;
		}
		.submitBtn{
			margin-top: 40rpx;
			width: 100%;
			height: 88rpx;
			border-radius: 4rpx;
			background-color: #1588FD;
			color: #FFFFFF;
			font-size: 32rpx;
			line-height: 88rpx;
			text-align: center;
		}
	}
</style>
