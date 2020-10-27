<template>
	<view class="history-index">
		<view class="h-head row verCenter">
			<view class="search-box row bothSide">
				<view class="search-bar row verCenter">
					<view class="country row verCenter">
						<text class="arrow"></text>
						<text class="txt">CHN 中国</text>
					</view>
					<input type="text" class="inp" placeholder="请输入企业名称关键词" placeholder-style="color:#999999;" />
				</view>
				<view class="btn row rowCenter verCenter">查一下</view>
			</view>
		</view>
		<view class="list">
			<view class="box">
				<text class="t1">LAVA INTERNATIONAL LIMITED INTERNATIONINTERNATIONINTERNATION</text>
				<view class="row verCenter">
					<text class="color1">非存续</text>
					<text class="line"></text>
					<text class="tt">印度 IND</text>
				</view>
				<text class="t2">企业经营地址：C-DDS/77,Sshubdbjejjnk Fhjdsj R jsjsj. 1587sj</text>
			</view>
			<view class="box">
				<text class="t1">LAVA INTERNATIONAL LIMITED INTERNATIONINTERNATIONINTERNATION</text>
				<view class="row verCenter">
					<text class="color1">非存续</text>
					<text class="line"></text>
					<text class="tt">印度 IND</text>
				</view>
				<text class="t2">企业经营地址：C-DDS/77,Sshubdbjejjnk Fhjdsj R jsjsj. 1587sj</text>
			</view>
			<view class="box">
				<text class="t1">LAVA INTERNATIONAL LIMITED INTERNATIONINTERNATIONINTERNATION</text>
				<view class="row verCenter">
					<text class="color2">非存续</text>
					<text class="line"></text>
					<text class="tt">印度 IND</text>
				</view>
				<text class="t2">企业经营地址：C-DDS/77,Sshubdbjejjnk Fhjdsj R jsjsj. 1587sj</text>
			</view>
			<view class="box">
				<text class="t1">LAVA INTERNATIONAL LIMITED INTERNATIONINTERNATIONINTERNATION</text>
				<view class="row verCenter">
					<text class="color1">非存续</text>
					<text class="line"></text>
					<text class="tt">印度 IND</text>
				</view>
				<text class="t2">企业经营地址：C-DDS/77,Sshubdbjejjnk Fhjdsj R jsjsj. 1587sj</text>
			</view>
			<view class="box">
				<text class="t1">LAVA INTERNATIONAL LIMITED INTERNATIONINTERNATIONINTERNATION</text>
				<view class="row verCenter">
					<text class="color1">非存续</text>
					<text class="line"></text>
					<text class="tt">印度 IND</text>
				</view>
				<text class="t2">企业经营地址：C-DDS/77,Sshubdbjejjnk Fhjdsj R jsjsj. 1587sj</text>
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
@import '../../assets/css/search/index.scss';
</style>
