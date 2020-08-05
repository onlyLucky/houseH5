<template>
	<view class="lease">
		<view class="lease-box">
			<lease-item></lease-item>
			<lease-item></lease-item>
			<lease-item></lease-item>
			<lease-item></lease-item>
			<lease-item></lease-item>
			<lease-item></lease-item>
		</view>
	</view>
</template>

<script>
	import leaseItem from "./leaseItem.vue"
	export default {
		components:{
			leaseItem
		}
	}
</script>

<style scoped>
</style>
