<template>
	<view class="login-page">
		<!-- html5 (增加语义化和可读性) -->
		<common-header :title="title"></common-header>
		
		<main class="main">
			<!-- 登录的表单 --> 
			<!-- <div></div> <span></span> -->
			<view class="label-value">
				<text>用户名</text>
				<u-input v-model="loginForm.username"></u-input>
			</view>
			<view class="label-value">
				<text>密码</text>
				<u-input v-model="loginForm.password"></u-input>
			</view>
		</main>
		
		<footer class="footer">
			<u-button type="primary" @click="submitLogin">提交</u-button>
		</footer>
	</view>
</template>

<script>
	// import CommonHeader from '@/components/CommonHeader/index.vue'
	
	export default {
		// components: {
		// 	CommonHeader
		// },
		data() {
			return {
				title: '登录',
				loginForm: {
					username: null,
					password: null
				}
			}
		},
		methods: {
			submitLogin() {
				// 调接口的操作
			}
		}
	}
</script>

<style lang="scss" scoped>
	.login-page {
		width: 100%;
		height: 100vh;
		position: relative;
		
		// 登录的表单
		.main {
			width: calc(100% - 100rpx);  // 动态的
			position: absolute;
			left: 50rpx;
			top: 300rpx;
			background: #eaeaea;
			border-radius: 20rpx;
			height: 300rpx;
			padding: 30rpx 24rpx;  // 盒子模型 => ie 正常
			box-sizing: border-box;  // 正常
		}
		
		.footer {
			width: calc(100% - 100rpx);
			position: fixed;
			bottom: 100rpx;
			left: 50rpx;
		}
	}
</style>
