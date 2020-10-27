<template>
	<view class="login-box">
		<view class="title column">
			<text class="t1">你好，</text>
			<text class="t1">欢迎使用外贸护法！</text>
		</view>
		<view class="form-box">
			<view class="form-type row verCenter bothSide">
				<view class="code row rowCenter verCenter">+ 86</view>
				<input type="text" value="" placeholder="请输入手机号码" class="inp" placeholder-style="color:#999999;" />
			</view>
			<view class="form-input row verCenter bothSide">
				<input type="text" value="" placeholder="请输入验证码" class="inp" placeholder-style="color:#999999;" />
				<button class="code">获取验证码</button>
			</view>
		</view>
		<view class="btn row verCenter rowCenter disabled">提交</view>
	</view>
</template>

<script>
import { API } from '@/util/api.js';
export default {
	data() {
		return {};
	},
	onLoad(options) {},
	methods: {}
};
</script>

<style scoped lang="scss">
@import '../../assets/css/user/login.scss';
</style>
