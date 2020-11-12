<template>
	<view class="contact">
		<image class="img" src="http://www.itcast.cn/2018czydz/images/gywmban.jpg"></image>
		<view class="info">
			<view @click="phone">联系电话：13412345678 ( 点击拨打 )</view>
			<view>地址：浙江省杭州市西湖风景区</view>
		</view>
		<map class="map" :longitude="longitude" :scale="scale" :latitude="latitude" :markers="markers"></map>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				longitude: 120.12792,
				latitude: 30.228932,
				scale: 13,
				markers:[
					{
						longitude: 120.12792,
						latitude: 30.228932,
						iconPath: '../../static/xh.png',
						width: 40,
						height: 40
					}
				]
			}
		},
		methods: {
			phone() {
				uni.makePhoneCall({
					phoneNumber: '1341234567'
				})
			}
		}
	}
</script>

<style lang="scss">
.contact{
	.img{
		width: 750rpx;
		height: 320rpx;
	}
	.info{
		padding: 10rpx 20rpx;
		font-size: 30rpx;
		view{
			line-height: 80rpx;
			border-bottom: 1px solid #eee;
		}
	}
	
	.map{
		width: 750rpx;
		height: 750rpx;
	}
}
</style>
