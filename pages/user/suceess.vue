<template>
	<view class="pay-success column">
		<text class="ico"></text>
		<text class="t1">支付成功</text>
		<text class="t2">请在收到手机短信或邮件通知后，访问官网www.xxxx.com【登录个人中心】-【订单管理】-【查阅报告】。</text>
		<view class="btn row rowCenter verCenter" @click="submit()" hover-class="none">完成</view>
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
		}
	}
};
</script>

<style scoped lang="scss">
@import '../../assets/css/user/suceess.scss';
</style>
