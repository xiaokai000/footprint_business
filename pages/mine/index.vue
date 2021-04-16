<template>
	<view>
		<view style="height: 20rpx; background-color: #F4F4F4;"></view>
			<u-cell-group :border="false">
				<u-cell-item title="核销记录" @click='go("/pages/hexiao/record")' ></u-cell-item>
				<u-cell-item title="激活码申请记录"  @click='go("/pages/activate/record")'></u-cell-item>
				<u-cell-item title="验证码申请记录"  @click='go("/pages/verification/record")'></u-cell-item>
			</u-cell-group>
			<view style="height: 20rpx; background-color: #F4F4F4;"></view>
			<u-cell-group :border="false">

				<u-cell-item title="账号设置"></u-cell-item>
				<u-cell-item title="修改密码" @click='go("/pages/mine/password/password")'></u-cell-item>

			</u-cell-group>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				
			}
		},
		methods: {
			go(url){
				uni.navigateTo({
					url
				})
			}
		}
	}
</script>

<style>

</style>
