<template>
	<view class="container">

			<view class="u-text-center main-text-40 font-weight-bold" style="margin-top: 40rpx;">
				脚印智趣游商家版
			</view>
			
			<view style="padding: 30rpx;">
				<view class="item" style="margin-top: 200rpx;">
					<u-input v-model="username"  :border="false" placeholder="用户名" />
				</view>
				<view class="item" style="margin-top: 40rpx;">
					<u-input v-model="password" type="password" placeholder="密码"  :border="false" />
				</view>
			</view>

			<view style="height: 100rpx;"></view>
			<bottom-btn text="登 录"></bottom-btn>

	</view>
</template>

<script>
	export default {
		data() {
			return {
				username: '',
				password: ''
			}
		},
		methods: {
			
		}
	}
</script>

<style scoped>
	.item{
		border-bottom: 1rpx solid #7FFFD4;
	}
</style>
