<template>
	<view class="buy">
		<view class="text  column">
			<text class="t1">LAVA INTERNATIONAL LIMITED TIONAL</text>
			<text class="t2">外贸护法企业编号：INDDUNSNUMBER</text>
			<text class="t3">经营地址：C-7/227, Second Floor Sector-7, Rohini Delhi DL 110085 IN,India</text>
			<view class="t4">
				如对服务内容有任何疑问，请咨询
				<text class="iconfont iconweikefu"></text>
				<text class="tt" @click="makePhoneCall()">客服：0755-23485853</text>
			</view>
		</view>
		<view class="title row verCenter">选择您需要的服务</view>
		<view class="content">
			<view class="tb">该企业建议购买深度信用报告,包含更丰富的企业数据以了解企业经营风险。</view>
			<view class="list row">
				<view class="box1 box" @click="type=2">
					<view class="bg" v-if="type == 1"></view>
					<view class="tit row verCenter">
						<template v-if="type == 2">
							<checkbox checked="true"/>
						</template>
						<template v-else>
							<checkbox/>
						</template>
						<text>深度信用报告</text>
					</view>
					<view class="wrap">
						<view class="t-xb">
							<text class="t1">等待</text>
							<text class="t2">5-10工作日</text>
							<text class="t1">获取</text>
							<text class="t2">最新的企业报告</text>
						</view>
						<view class="baokuo">内容包括</view>
						<view class="ul-box">
							<view class="li">基础信息</view>
							<view class="li">股东信息</view>
							<view class="li">关联企业</view>
							<view class="li">付款逾期信息</view>
							<view class="li">风险诉讼信息</view>
							<view class="li">企业新闻记录</view>
							<view class="li">监管机构信息</view>
							<view class="li">变更记录</view>
							<view class="li">管理层信息</view>
							<view class="li">经营信息</view>
							<view class="li">财务状况</view>
							<view class="li">企业风险指标分析</view>
							<view class="li">竞争对手信息</view>
						</view>
					</view>
				</view>
				<view class="box2 box" @click="type=1">
					<view class="bg" v-if="type == 2"></view>
					<view class="tit row verCenter">
						<template v-if="type == 1">
							<checkbox checked="true"/>
						</template>
						<template v-else>
							<checkbox/>
						</template>
						<text>风险决策报告</text>
					</view>
					<view class="wrap">
						<view class="t-xb colu">
							<text class="t1">立即获取</text>
							<text class="t2">2018年12月12日企业报告</text>
						</view>
						<view class="baokuo">内容包括</view>
						<view class="ul-box">
							<view class="li">基础信息</view>
							<view class="li">关联企业</view>
							<view class="li">财务状况</view>
							<view class="li">竞争对手信息</view>
							<view class="li">管理层信息</view>
							<view class="li">经营信息</view>
							<view class="li">风险诉讼信息</view>
							<view class="li">监管机构信息</view>
						</view>
					</view>
				</view>
			</view>
			<view class="tip row">
				<text class="iconfont icontishi1"></text>
				<text class="tip-t">因各国政策法规及公司自身经营原因，无法保证获取上述所有数据。</text>
			</view>
		</view>
		<view class="pay-btn row bothSide">
			<view class="bar row verCenter">
				<text class="t1">应付总额：</text>
				<text class="t2">
					<template v-if="type == 2">899</template>
					<template v-if="type == 1">399</template>
				</text>
				<text class="t3">元</text>
			</view>
			<view class="btn row rowCenter verCenter" @click="pay()">支付</view>
		</view>
	</view>
</template>

<script>
import { API } from '@/util/api.js';

export default {
	data() {
		return {
			type: 2
		};
	},
	onLoad(options) {},
	methods: {
		makePhoneCall() {
			uni.makePhoneCall({
				phoneNumber: '0755-23485853'
			});
		},
		pay() {
			uni.navigateTo({
				url: '/pages/user/pay'
			});
		}
	}
};
</script>

<style scoped lang="scss">
@import '../../assets/css/user/buy.scss';
</style>
