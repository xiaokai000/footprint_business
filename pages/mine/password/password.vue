<template>
	<view class="container">
		<view style="margin-bottom: 300rpx;">
			<u-form model="form" ref="uForm">
			
				<u-form-item  label-width="150"  label="当前密码"  :border-bottom="false">
					<u-input :border="true" type="number" placeholder="请输入当前密码" v-model="form.old_password" ></u-input>
				</u-form-item>
				<u-form-item  label-width="150"  label="新密码"  :border-bottom="false">
					<u-input :border="true" type="number" placeholder="请输入新密码" v-model="form.new_password" ></u-input>
				</u-form-item>
				<u-form-item  label-width="150"  label="确认密码"  :border-bottom="false">
					<u-input :border="true" type="number" placeholder="请确认密码" v-model="form.confirm_password" ></u-input>
				</u-form-item>
						
			</u-form>
		</view>

		<bottom-btn backgroundColor="#1E90FF" @click="goRecord" text="保存" ></bottom-btn>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				form: {
					old_password: '',
					new_password: '',
					confirm_password: ''
				}
			}
		},
		methods: {
			
		}
	}
</script>

<style>

</style>
