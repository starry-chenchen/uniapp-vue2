<script>
export default {
	onLaunch: function () {
		console.log('App Launch');
	},
	onShow: function () {
		console.log('App Show');
	},
	onHide: function () {
		console.log('App Hide');
	}
};
</script>

<style lang="scss">
@import '@/uni_modules/uview-ui/index.scss';
/*每个页面公共css */
page {
	padding: 32rpx;
}

input {
	margin: 24rpx 0;
	padding: 20rpx;
	border: 2rpx solid #ccc;
	border-radius: 8rpx;
}
</style>
