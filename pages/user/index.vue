<template>
	<view class="user-index">
		<view class="user-head column">
			<view class="tel row verCenter">
				<text class="iconfont iconweikefu"></text>
				<text class="tel-t1" @click="makePhoneCall()">客服：0755-23485853</text>
			</view>
			<view class="ad"><image src="http://img.ichunt.com/images/ichunt/minProgram/bcaf917ddb6a16e9dc72cbfa3d9edb35.jpg" mode="aspectFill"></image></view>
			<text class="t1">Skjdi.1234</text>
			<view class="row rowCenter">
				<text class="t2">手机号：13827272626</text>
				<text class="t3">（未认证）</text>
			</view>
		</view>
		<view class="content">
			<view class="tab row  verCenter">
				<view @click="tab(index)" :class="{ curr: active == index }" v-for="(item, index) in itemtext" :key="index" class="box row rowCenter verCenter">{{ item }}</view>
			</view>
			<view class="collection" :style="{ display: isAvisible }">
				<view class="box row bothSide">
					<text class="text">LAVA INTERNATIONAL LIMITEDINTERNATIONLIMITEDINTERNATIONLIMITEDINTERNATIONLIMITEDINTERNATIONLIMITEDINTERNATIONLIMITEDINTERNATION</text>
					<view class="right-bar column">
						<text class="t1">美国 USA</text>
						<text class="iconfont iconqianjin"></text>
					</view>
				</view>
				<view class="box row bothSide">
					<text class="text">LAVA INTERNATIONAL LIMITEDINTERNATIONLIMITEDINTERNATIONLIMITEDINTERNATIONLIMITEDINTERNATIONLIMITEDINTERNATIONLIMITEDINTERNATION</text>
					<view class="right-bar column">
						<text class="t1">美国 USA</text>
						<text class="iconfont iconqianjin"></text>
					</view>
				</view>
				<view class="box row bothSide">
					<text class="text">LAVA INTERNATIONAL LIMITEDINTERNATIONLIMITEDINTERNATIONLIMITEDINTERNATIONLIMITEDINTERNATIONLIMITEDINTERNATIONLIMITEDINTERNATION</text>
					<view class="right-bar column">
						<text class="t1">美国 USA</text>
						<text class="iconfont iconqianjin"></text>
					</view>
				</view>
			</view>
			<view class="list-order" :style="{ display: isBvisible }">
				<view class="tip row">
					<text class="iconfont iconjinggao"></text>
					<text class="t1">报告完成通知-访问官网wwww.xxxx.com【登录个人中心】-【订单管理】-【查阅报告】为获得更好的阅读体验，建议您使用个人电脑查阅</text>
				</view>
				<view class="box column">
					<text class="t1">LAVA INTERNATIONAL LIMITED INTERNATION…</text>
					<text class="color1">深度信用风险报告</text>
					<view class="row bothSide">
						<text class="t2">订单完成时间：2020年6月12日</text>
						<view><text class="t3">订单状态：已完成</text></view>
					</view>
				</view>
				<view class="box column">
					<text class="t1">LAVA INTERNATIONAL LIMITED INTERNATION…</text>
					<text class="color2">深度信用风险报告</text>
					<view class="row bothSide">
						<text class="t2">订单完成时间：2020年6月12日</text>
						<view>
							<text class="t3">订单状态：</text>
							<text class="t4">未完成</text>
						</view>
					</view>
				</view>
				<view class="box column">
					<text class="t1">LAVA INTERNATIONAL LIMITED INTERNATION…</text>
					<text class="color2">深度信用风险报告</text>
					<view class="row bothSide">
						<text class="t2">订单完成时间：2020年6月12日</text>
						<view>
							<text class="t3">订单状态：</text>
							<text class="t4">未完成</text>
						</view>
					</view>
				</view>
				<view class="box column">
					<text class="t1">LAVA INTERNATIONAL LIMITED INTERNATION…</text>
					<text class="color2">深度信用风险报告</text>
					<view class="row bothSide">
						<text class="t2">订单完成时间：2020年6月12日</text>
						<view>
							<text class="t3">订单状态：</text>
							<text class="t4">未完成</text>
						</view>
					</view>
				</view>
				<view class="box column">
					<text class="t1">LAVA INTERNATIONAL LIMITED INTERNATION…</text>
					<text class="color2">深度信用风险报告</text>
					<view class="row bothSide">
						<text class="t2">订单完成时间：2020年6月12日</text>
						<view>
							<text class="t3">订单状态：</text>
							<text class="t4">未完成</text>
						</view>
					</view>
				</view>
			</view>
		</view>
	</view>
</template>

<script>
import { API } from '@/util/api.js';
export default {
	data() {
		return {
			itemtext: ['我的收藏', '我的订单'],
			active: 0,
			isAvisible: 'block',
			isBvisible: 'none'
		};
	},
	onLoad(options) {
		let type=uni.getStorageSync('type');
		if(type == 1){
			this.active=1;
			this.isAvisible = 'none';
			this.isBvisible = 'block';
		}
	},
	methods: {
		makePhoneCall() {
			uni.makePhoneCall({
				phoneNumber: '0755-23485853'
			});
		},
		tab(index) {
			this.active = index;
			this.isAvisible = 'none';
			this.isBvisible = 'none';
			if (index == 0) {
				index == 0 ? (this.isAvisible = 'block') : (this.isAvisible = 'none');
			} else if (index == 1) {
				index == 1 ? (this.isBvisible = 'block') : (this.isBvisible = 'none');
			}
		}
	}
};
</script>

<style scoped lang="scss">
@import '../../assets/css/user/index.scss';
</style>
