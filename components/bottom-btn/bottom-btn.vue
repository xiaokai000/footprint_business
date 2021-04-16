<template>
	<view class="out">
		<view :class="{bottomBtn: true, border: border}" :style="{backgroundColor: backgroundColor, width: width, height: height}" @click="click">
			{{ text }}
		</view>
		
	</view>
</template>

<script>
	export default {
		props:{
			text: {
				type: String,
				default: '确认'
			},
			border: {
				type: Boolean,
				default: false
			},
			width: {
				type: String,
				default: '88vw'
			},
			height: {
				type: String,
				default: '80rpx'
			},
			backgroundColor: {
				type: String,
				default: '#7FFFD4'
			},
			
		},

		data() {
			return {
				
			}
		},
		methods: {
			click(){
				this.$emit('click')
			}

		}
	}
</script>

<style>

	.out {
		display:flex;
		justify-content: center;
		align-items: center;
		color: #FFFFFF;
	}

	.bottomBtn {		
		border-radius: 40rpx;
		font-weight: bold;
		display:flex;
		justify-content: center;
		align-items: center;

	}
	.border {

		border: 1px solid #333333;
	}

</style>
