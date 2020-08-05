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
			<view v-show="false">
				<lease></lease>
			</view>
			<view v-show="false">
				<contract></contract>
			</view>
		</view>
	</view>
</template>

<script>
	import check from "./commponts/check.vue"
	import lease from "./commponts/lease.vue"
	import contract from "./commponts/contract.vue"
	export default {
		components:{
			check,
			lease,
			contract
		},
		onLoad() {
			this.getlocations()
		},
		data() {
			return {
				
			}
		},
		methods: {
			getlocations() {
				console.log('xing')
				wx.getLocation({
				  type: 'wgs84', // 默认为wgs84的gps坐标，如果要返回直接给openLocation用的火星坐标，可传入'gcj02'
				  success: function (res) {
				    var latitude = res.latitude; // 纬度，浮点数，范围为90 ~ -90
				    var longitude = res.longitude; // 经度，浮点数，范围为180 ~ -180。
				    var speed = res.speed; // 速度，以米/每秒计
				    var accuracy = res.accuracy; // 位置精度
				  }
				});
			}
		},
		
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
		position: fixed;
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
	.tabContent-box{
		padding-top: 100rpx;
	}
</style>
