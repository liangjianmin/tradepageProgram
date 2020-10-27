<template>
	<view class="h-index">
		<view class="h-head column verCenter">
			<view class="top row bothSide verCenter">
				<image src="../../static/logo.png" mode="aspectFill" class="logo"></image>
				<view class="row verCenter">
					<text class="iconfont iconweikefu"></text>
					<text class="tel">客服：0755-23485853</text>
				</view>
			</view>
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
			<view class="promt">
				<text class="txt">温馨提醒</text>
				<text class="iconfont iconqianjin"></text>
			</view>
		</view>
		<view class="content">
			<view class="title row verCenter">
				<text class="t1">最近搜索</text>
				<view class="t2 row rowCenter verCenter">
					<text class="iconfont iconhuaban"></text>
					<text>会员产品权益</text>
				</view>
			</view>
			<view class="recently">
				<view class="box row bothSide verCenter">
					<text class="t1">SKY PHONE LIC SKY.  USA</text>
					<text class="t2">USA</text>
				</view>
				<view class="box row bothSide verCenter">
					<text class="t1">LALS YHhhddkc hJYGGCF hVAHD</text>
					<text class="t2">HK</text>
				</view>
				<view class="box row bothSide verCenter">
					<text class="t1">SKY PHONE LIC SKY.  USA</text>
					<text class="t2">USA</text>
				</view>
				<view class="box row bothSide verCenter">
					<text class="t1">青岛华正信息科技有限公司</text>
					<text class="t2">中国</text>
				</view>
			</view>
			<view class="list">
				<view class="box column">
					<text class="t1">Google Gdjadb inc.</text>
					<view class="row verCenter">
						<text class="color1">非存续</text>
						<text class="line"></text>
						<text class="tt">印度 IND</text>
					</view>
					<text class="t2">员工数量：4500</text>
					<text class="t2">销售收入：$64,451,260.00 （大型企业）</text>
					<text class="t2">领导人：拉吉库马尔·希拉尼</text>
				</view>
				<view class="box column">
					<text class="t1">Google Gdjadb inc.</text>
					<view class="row verCenter">
						<text class="color2">非存续</text>
						<text class="line"></text>
						<text class="tt">印度 IND</text>
					</view>
					<view class="row verCenter">
						<text class="t3">国家 / 地区风险等级：</text>
						<text class="level row rowCenter verCenter">8</text>
						<text class="color">高风险</text>
						<text class="iconfont icontishi"></text>
					</view>
					<view class="row verCenter">
						<text class="t3">国家 / 地区主权信用风险等级：</text>
						<text class="level row rowCenter verCenter">C</text>
						<text class="color">高风险</text>
						<text class="iconfont icontishi"></text>
					</view>
					<text class="t2">销售收入：$451,260.00 （小型企业）</text>
				</view>
			</view>
		</view>
		<view class="risk">
			<image src="../../static/p1.png" mode="aspectFill"></image>
		</view>
		<view class="agreement row bothSide verCenter">
			<text class="txt">《用户协议》</text>
			<text class="iconfont iconguanbi"></text>
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
