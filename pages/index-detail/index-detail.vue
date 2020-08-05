<template>
	<view class="message">
		<view class="tab-box">
			<view class="tab-item active">租约信息</view>
			<view class="tab-item">账单信息</view>
			<view class="tab-item">合同信息</view>
		</view>
		<view class="tabContent-box">
			<view v-show="true">
				<check></check>
			</view>
		</view>
	</view>
</template>

<script>
	import check from "./commponts/check.vue"
	export default {
		components:{
			check
		},
		data() {
			return {
				
			}
		},
		methods: {
			
		}
	}
</script>

<style lang="less" scoped>
	.message{
		width: 100vw;
		height: 100vh;
		background-color: #F7F8FA;
	}
	.tab-box{
		width: 100%;
		height: 90rpx;
		background-color: #FFFFFF;
		position: flex;
		display: flex;
		align-items: center;
		justify-content: space-evenly;
		top: 0rpx;
		.tab-item{
			font-size: 30rpx;
			line-height: 90rpx;
			text-align: center;
			white-space: nowrap;
		}
		.tab-item.active{
			color: #1588FD;
			border-bottom: 1rpx solid #1588FD;
		}
	}
</style>
