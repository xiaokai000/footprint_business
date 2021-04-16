<template>
	<view class="container">
		<view style="margin-bottom: 300rpx;">
			<u-form  ref="uForm">
			
				<u-form-item  label="游戏名称"  label-width="150" :border-bottom="false">
					<u-input :border="true" type="select" :select-open="selectShow" v-model="gameName" placeholder="请选择" @click="selectShow = true"></u-input>
				</u-form-item>
				<u-form-item  label-width="150"  label="申请数量"  :border-bottom="false">
					<u-input :border="true" type="number" placeholder="请输入申请数量" v-model="number" ></u-input>
				</u-form-item>
	
				
			</u-form>
			<u-select mode="single-column" :list="selectList" v-model="selectShow" @confirm="selectConfirm"></u-select>
		</view>

		
		<bottom-btn style="color: #FFFFFF;" backgroundColor="#1E90FF" @click="goRecord"  ></bottom-btn>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				selectShow: false,
				gameName: '',
				number: '',
				selectList: [
					{
						value: 'LOL',
						label: 'LOL'
					},
					{
						value: 'DNF',
						label: 'DNF'
					},
					{
						value: 'CF',
						label: 'CF'
					}
				],
			}
		},
		methods: {
			selectConfirm(e){
				this.gameName =  e[0].label
			},
			goRecord(){
				
				if(this.gameName == ''){
					uni.showToast({
						title:'请选择游戏',
						icon: 'none'
					})
					return
				}
				if(this.number == ''){
					uni.showToast({
						title:'请输入数量',
						icon: 'none'
					})
					return
				}
				
				uni.showToast({
					title:'已生成，请去激活码申请记录中查看',
					icon: 'none'
				})
			}
		}
	}
</script>

<style>

</style>
