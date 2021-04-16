<template>
	<view class="container">
		<view style="margin-bottom: 300rpx;">
			<u-form  ref="uForm">
			
				<u-form-item  label="游戏名称" prop="goodsType" label-width="150" :border-bottom="false">
					<u-input :border="true" type="select" :select-open="selectShow" v-model="gameName" placeholder="请选择" @click="selectShow = true"></u-input>
				</u-form-item>
			</u-form>
			<u-select mode="single-column" :list="selectList" v-model="selectShow" @confirm="selectConfirm"></u-select>
		</view>

		
		<bottom-btn backgroundColor="#1E90FF"  ></bottom-btn>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				selectShow: false,
				gameName: '',
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
			}
		}
	}
</script>

<style>

</style>
