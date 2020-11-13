<template>
	<view class="pay-box">
		<view class="text column">
			<text class="t1">为提供更好的服务，请核对本次您的联系方式。以便我们的工作人员与您核对企业信息并发放企业报告通知。</text>
			<view>
				<text class="t2">如对服务内容有任何疑问，请咨询</text>
				<text class="iconfont iconweikefu"></text>
				<text class="t3" @click="makePhoneCall()">客服：0755-23485853</text>
			</view>
		</view>
		<view class="contact">
			<view class="input-box row bothSide verCenter mb">
				<text class="t1">联系电话</text>
				<input type="text" placeholder="请输入手机号码" placeholder-style="color:#999999;" class="inp"/>
			</view>
			<view class="input-box row bothSide verCenter">
				<text class="t1">联系邮箱</text>
				<input type="text" placeholder="请输入联系邮箱" placeholder-style="color:#999999;" class="inp"/>
			</view>
		</view>
		<view class="invoice row bothSide verCenter">
			<text class="t1">发票</text>
			<text class="t2">订单完成后，可在外贸护法网页端个人中心开具发票。</text>
		</view>
		<view class="tgb row">
			<text class="t1">查看报告</text>
			<view class="t2 column">
				<text>报告完成通知-访问官网wwww.xxxx.com【登录个人中心】-【订单管理】-【查阅报告】</text>
				<text>为获得更好的阅读体验，建议您使用个人电脑查阅</text>
			</view>
		</view>
		<view class="agreement row">
			 <checkbox value="cb"  class="check" />
			 <navigator class="txt" url="/pages/user/agreement" hover-class="none">已阅读并同意《用户协议》《隐私权政策》《版权声明》《免责声明》</navigator>
		</view>
		<view class="pay-btn row bothSide">
			<view class="bar row verCenter">
				<text class="t1">应付总额：</text>
				<text class="t2">899</text>
				<text class="t3">元</text>
			</view>
			<view class="btn row rowCenter verCenter" @click="submit()">支付</view>
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
	methods: {
		submit(){
			uni.switchTab({
				url:'/pages/user/index'
			})
			uni.setStorageSync('type', 1);
		},
		makePhoneCall() {
			uni.makePhoneCall({
				phoneNumber: '0755-23485853'
			});
		}
	}
};
</script>

<style scoped lang="scss">
@import '../../assets/css/user/pay.scss';
</style>
