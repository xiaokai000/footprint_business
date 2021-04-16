<template>
	<view>
		
		<view style="padding: 20rpx;">
			<view class="item">
				<view>古北水镇探秘</view>
				<view>待激活</view>
			</view>
			<view class="item">
				<view>ID：1234455367</view>
				<view>50元</view>
			</view>
			<view class="item">
				<view>核销时间：2020-06-17 10:00:00</view>
			</view>
		</view>

		
		
		<view class="u-flex  u-col-center " style="flex-direction: column; margin-top: 50px;">
			<view style="font-size: 18px;">请向客户出示激活码</view>
			<view class="qrcode" ref="qrCodeUrl" style="height: auto; margin-top: 50rpx;" >
				<canvas canvas-id="qrcode" :style="{ width: canvasWidth + 'px', height: canvasHeight + 'px' }" />
			</view>
			<bottom-btn style="margin-top: 100rpx;" backgroundColor="#1E90FF" width="70vw" text="确认并返回"></bottom-btn>
			
		</view>
		
		
	</view>
</template>

<script>
	import uQRCode from '@/js_sdk/uqrcode.js'
	export default {
		data() {
			return {
				canvasWidth: 200,
				canvasHeight: 200,
			}
		},
		onLoad() {
				this.makeQrCode()
		},
		methods: {
			makeQrCode() {
				uQRCode.make({
					canvasId: 'qrcode',
					componentInstance: this,
					text: 'test',
					size: this.canvasWidth,
					margin: 10,
					backgroundColor: '#ffffff',
					foregroundColor: '#000000',
					fileType: 'jpg',
					correctLevel: uQRCode.errorCorrectLevel.H,
					success: res => {
						console.log(res)
					}
				})
			},
		}
	}
</script>

<style scoped>
	.item {
		display: flex;
		justify-content: space-between;
		margin-top: 20px;
	}
</style>
