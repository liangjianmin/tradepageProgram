<template>
	<view class="h-index">home</view>
</template>

<script>
import { API } from '@/util/api.js';

export default {
	data() {
		return {};
	},
	onLoad(options) {},
	onShow() {},
	onPullDownRefresh() {
		this.refresh();
	},
	methods: {
		getData() {},
		refresh() {
			uni.stopPullDownRefresh();
			this.getData();
		}
	}
};
</script>

<style scoped lang="scss">
@import '../../assets/css/index/index.scss';
</style>
