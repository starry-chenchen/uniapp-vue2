<template>
	<view class="page">
		<h3>物流信息录入</h3>
		<input type="text" placeholder="请输入物流单号" />
		<!-- <button open-type="getPhoneNumber" @getphonenumber="getPhoneNumber">唤起授权</button>
		<button @click="getUserInfo">获取用户信息</button> -->
	</view>
</template>

<script>
export default {
	data() {
		return {
			title: 'Hello',
			provider: 'weixin'
		};
	},
	onLoad() {
		uni.login({
			provider: this.provider, //使用微信登录
			onlyAuthorize: true,
			success(res) {
				const { code } = res;
				// 微信登录成功 已拿到code
				if (code) {
					uni.request({
						url: 'https://api.weixin.qq.com/sns/jscode2session',
						data: {
							appid: 'wx51fd1d0acabb0131',
							secret: '1ef380bc02c13b1eebb0afb0e5486f6d',
							js_code: code,
							grant_type: 'authorization_code'
						},
						success(sRes) {
							console.log('sRes', sRes);
						}
					});
				} else {
					console.log('登录失败！' + res.errMsg);
				}
			}
		});
	},
	methods: {
		getPhoneNumber(e) {},
		// 获取用户信息
		getUserInfo() {
			uni.getUserInfo({
				provider: this.provider,
				success(res) {
					console.log('res', res);
				}
			});
		}
	}
};
</script>

<style lang="scss" scoped></style>
