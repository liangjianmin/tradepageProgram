<template>
	<view class="h-index">
		<view class="h-head column verCenter">
			<view class="top row bothSide">
				<image src="../../static/logo.png" mode="aspectFill"></image>
				<view class="row verCenter">
					<text class="iconfont iconweikefu"></text>
					<text class="tel">客服：0755-23485853</text>
				</view>
			</view>
		</view>
	</view>
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
