<template>
	<view class="history">
		<view class="search row bothSide verCenter">
			<view class="search-bar row bothSide verCenter">
				<view class="row verCenter">
					<text class="iconfont iconsearch"></text>
					<input type="text" placeholder=""  class="inp" />
				</view>
				<text class="iconfont iconguanbi"></text>
			</view>
			<text class="btn" @click="canel()">取消</text>
		</view>
		<view class="title row bothSide">
			<text class="t1">历史记录</text>
			<text class="t2">清空</text>
		</view>
		<view class="list">
			<view class="box row verCenter">SKY PHONE LIC. USA</view>
			<view class="box row verCenter">SKY PHONE</view>
			<view class="box row verCenter">SKY PHONE LIC. USASKY PHONE LIC.</view>
			<view class="box row verCenter">SKY PHONE LIC. USA</view>
			<view class="box row verCenter">SKY PHONE LIC.</view>
		</view>
	</view>
</template>

<script>
import { API } from '@/util/api.js';

export default {
	data() {
		return {
			name: ''
		};
	},
	onLoad(options) {
		this.name = options.name || '';
	},
	onShow() {},
	onPullDownRefresh() {
		this.refresh();
	},
	methods: {
		getData() {},
		canel() {
			uni.switchTab({
				url: '/pages/index/index'
			});
		},
		refresh() {
			uni.stopPullDownRefresh();
			this.getData();
		}
	}
};
</script>

<style scoped lang="scss">
@import '../../assets/css/search/history.scss';
</style>
