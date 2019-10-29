<template>
	<view class="content">
		<image class="logo" src="/static/logo.png"></image>
		<view class="text-area">
			<form @submit="login">
				<div>
					<label>用户名: </label>
					<input type="text" name="name"/>
				</div>
				<div>
					<label>密码: </label>
					<input type="password" name="passwd"/>
				</div>
				<div>
					<button form-type="submit">登陆</button>
				</div>
			</form>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				title: 'Hello'
			}
		},
		onLoad() {

		},
		methods: {
			login: function(e) {
				var formdata = e.detail.value;
				uni.request({
				    url: 'http://127.0.0.1:8080/login', //仅为示例，并非真实接口地址。
				    data: formdata,
				    header: {
				        'custom-header': 'hello' //自定义请求头信息
				    },
				    success: (res) => {
						if(res.data.result) {
							uni.navigateTo({
								url: '/pages/myindex/index'
							})
						}
				    }
				});
			}
		}
	}
</script>

<style>
	.content {
		display: flex;
		flex-direction: column;
		align-items: center;
		justify-content: center;
	}

	.logo {
		height: 200rpx;
		width: 200rpx;
		margin-top: 200rpx;
		margin-left: auto;
		margin-right: auto;
		margin-bottom: 50rpx;
	}

	.text-area {
		display: flex;
		justify-content: center;
	}

	.title {
		font-size: 36rpx;
		color: #8f8f94;
	}
	
	.form {
		width : 100%
	}
</style>
