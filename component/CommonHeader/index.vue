<template>
	<view>
		<header class="header">
			<!-- 图片 -->
			<!-- 相对路径（从'/'开始） -->
			<image class="back" src="/static/logo.png" mode=""></image>
			<view class="title">{{ title }}</view>
		</header>
	</view>
</template>

<script>
	export default {
		name: 'commonHeader',
		props: {
			title: {
				type: String,
				default: ''
			}
		},
		data() {
			return {
				
			}
		}
	}
</script>

<style lang="scss" scoped>
	.header {
		width: 100%;
		line-height: 88rpx;
		text-align: center;
		position: relative; // 相对
		border-bottom: 1rpx solid #eaeaea;
		
		.back {
			width: 30rpx;
			height: 30rpx;
			position: absolute;
			top: 30rpx;
			left: 24rpx;
		}
		.title {
			font-size: 30rpx;
			color: #1890ff;
			font-weight: 600;
		}
	}
</style>