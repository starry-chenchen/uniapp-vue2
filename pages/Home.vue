<template>
	<view class="page">
		<input type="text" placeholder="请输入单号查询" />

		<uni-list>
			<uni-list-item title="uni-app" note="12314">
				<template #body>
					<text>我是第一行文字</text>
				</template>
			</uni-list-item>
			<uni-list-item title="uni-app" note="12314"></uni-list-item>
		</uni-list>
	</view>
</template>

<script>
export default {
	data() {
		return {
			list: []
		};
	},
	methods: {}
};
</script>

<style lang="scss" scoped></style>
