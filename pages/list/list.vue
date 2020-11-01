<template>
	<view>
		列表页
		<view class="item" v-for="(item,index) in list" :key="index">{{item}}</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				list: ['打了飞机','阿道夫','大是大非','打了飞机','阿道夫','大是大非','打了飞机','阿道夫','大是大非']
			};
		},
		onPullDownRefresh() {
			setTimeout(()=>{
				this.list.push('23234adf ')
				uni.stopPullDownRefresh()
			},500)
			console.log(11111)
		},
		onReachBottom() {
			setTimeout(()=>{
				this.list.push('23333333333 ')
			},500)
			console.log(22222222222)
		}
	}
</script>

<style lang="scss">
.item{
	line-height: 100rpx;
}
</style>
