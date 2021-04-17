<template>
	<view class="u-flex u-row-center u-col-center " style="flex-direction: column; height: 100vh;">
		<view class="item yzm" style="flex-direction: column; width: 350px;" @click="verification">
			<view >申请验证码</view>
			<view class="circle" >
				<img src="/static/images/u64.svg" alt="">
			</view>
		</view>
		<view class="u-flex item" style="width: 350px; justify-content: space-between; margin-top: 10px;">

			
			<view class="hxm item" style="flex-direction: column;" @click="scan">
				<view >扫码核销</view>
				<view class="circle" >
					<img src="/static/images/u22.svg" alt="" style="width: 43px; height: 43px;">
				</view>
			</view>
			<view class="jhm item" style="flex-direction: column;" @click="activate">
				<view >申请激活码</view>
				<view class="circle" >
					<img src="/static/images/u23.svg" alt="">
				</view>
			</view>
			
		</view>
		
	</view>
</template>

<script>
	export default {
		data() {
			return {
				
			}
		},
		methods: {
			scan(){
				uni.scanCode({
				    onlyFromCamera: true,
				    success: function (res) {
				        uni.navigateTo({
				        	url: '../hexiao/index'
				        })
				    }
				});

			},
			activate(){
				uni.navigateTo({
					url: '/pages/activate/index'
				})
			},
			verification (){
				uni.navigateTo({
					url: '/pages/verification/index'
				})
			}
		}
	}
</script>

<style scoped>
	.item {
		height: 150px;
		border-radius: 6px;
		color: #FFFFFF;
		font-size: 28px;
		font-weight: 400;
		display: flex;
		justify-content: center;
		align-items: center;
	}
	.yzm {
		background: linear-gradient(180deg, rgba(236, 128, 141, 1) 0%, rgba(194, 128, 255, 1) 100%);
		
	}
	.hxm {
		background: linear-gradient(180deg, rgba(128, 128, 255, 1) 0%, rgba(194, 128, 255, 1) 100%);
		width: 170px;
	}
	.jhm {
		background: linear-gradient(180deg, rgba(34, 173, 232, 1) 0%, rgba(160, 229, 197, 1) 100%);
		width: 170px;
	}
	
	img {
		width: 59px;
		height: 59px;
	}
	.circle {
		height: 78px; 
		width: 78px; 
		margin-top: 10rpx;
		background-color: #FFFFFF; 
		border-radius: 39px;
		display: flex;
		justify-content: center;
		align-items: center;
		flex-direction: column;
	}
	
</style>
