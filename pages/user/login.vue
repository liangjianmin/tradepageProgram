<template>
	<view class="login-box">
		<view class="title column">
			<text class="t1">你好，</text>
			<text class="t1">欢迎使用外贸护法！</text>
		</view>
		<view class="form-box">
			<view class="form-type row verCenter bothSide">
				<view class="code row rowCenter verCenter">+ 86</view>
				<input type="text" value="" placeholder="请输入手机号码" class="inp" placeholder-style="color:#999999;" v-model="phone" />
			</view>
			<view class="form-input row verCenter bothSide">
				<input type="text" value="" placeholder="请输入验证码" class="inp" placeholder-style="color:#999999;" v-model="smsCode" />
				<button class="code" :value="codetext" @click="getCode()" :class="{ 'code-curr': codeactive }" :disabled="codeactive">{{ codetext }}</button>
			</view>
		</view>
		<view class="btn row verCenter rowCenter disabled" @click="submit">提交</view>
	</view>
</template>

<script>
import { API } from '@/util/api.js';
export default {
	data() {
		return {
			phone: '13456789875',
			smsCode: '1234',
			codetext: '获取验证码',
			codeactive: false
		};
	},
	onLoad(options) {},
	methods: {
		getCode() {
			var myreg = /^[1][3,4,5,7,8][0-9]{9}$/;

			if (!this.phone) {
				uni.showModal({
					title: '提示',
					content: '请输入手机号',
					showCancel: false
				});

				return;
			}

			if (!myreg.test(this.phone)) {
				uni.showModal({
					title: '提示',
					content: '请输入正确手机号',
					showCancel: false
				});

				return;
			}
			
			this.countdDown(); //倒计时开始 
		},
		countdDown() {
			var me = this;
			var wait = 60;
			me.disabled = true;
			me.codeactive = true;
			me.codetext = wait + '秒后获取';
			var clock = setInterval(doLoop, 1000);

			function doLoop() {
				wait--;
				if (wait > 0) {
					me.codetext = wait + '秒后获取';
					me.codeactive = true;
				} else {
					clearInterval(clock);
					me.disabled = false;
					me.codeactive = false;
					me.codetext = '重新获取';
					wait = 60;
				}
			}
		},
		submit() {
			var myreg = /^[1][3,4,5,7,8][0-9]{9}$/;

			if (!this.phone) {
				uni.showModal({
					title: '提示',
					content: '请输入手机号',
					showCancel: false
				});

				return;
			}

			if (!myreg.test(this.phone)) {
				uni.showModal({
					title: '提示',
					content: '请输入正确手机号',
					showCancel: false
				});

				return;
			}

			if (!this.smsCode) {
				uni.showModal({
					title: '提示',
					content: '请输入验证码',
					showCancel: false
				});

				return;
			}
			
			uni.navigateTo({
				url:'/pages/detail/index'
			})
		}
	}
};
</script>

<style scoped lang="scss">
@import '../../assets/css/user/login.scss';
</style>
