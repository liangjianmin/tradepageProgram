<template>
	<view class="detail">
		<view class="h-head row verCenter">
			<view class="search-box row bothSide">
				<view class="search-bar row verCenter">
					<view class="country row verCenter">
						<text class="arrow"></text>
						<text class="txt">CHN 中国</text>
					</view>
					<input type="text" class="inp" :value="name" placeholder="请输入企业名称关键词" placeholder-style="color:#999999;" />
				</view>
				<view class="btn row rowCenter verCenter">查一下</view>
			</view>
		</view>
		<view class="collection column">
			<text class="t1">LAVA INTERNATIONAL LIMITED TIONALTIONALTIONAL</text>
			<view class="list row">
				<view class="box color1 row rowCenter verCenter">国别风险高</view>
				<view class="box color1 row rowCenter verCenter">主权信用风险高</view>
				<view class="box color2 row rowCenter verCenter">主权信用风险中</view>
				<view class="box color3 row rowCenter verCenter">主权信用风险低</view>
			</view>
			<text class="t2">外贸护法企业编号：INDDUNSNUMBER</text>
			<text class="t3">信息更新时间：2019年10月1日；</text>
			<view class="btn-box row">
				<view class="btn row rowCenter verCenter">收藏企业</view>
			</view>
		</view>
		<view class="title row rowCenter verCenter" style="width: 150rpx;">基本信息</view>
		<!-- 基本信息 -->
		<view class="baseinfo">
			<view class="show-data row">
				<view class="box column">
					<text class="t1">注册编号</text>
					<text class="t2">U32201DL2009PLC188920</text>
					<text class="t1">营业日期</text>
					<text class="t2">2009年3月27日</text>
					<text class="t1">电话</text>
					<text class="t2">18589050841</text>
					<text class="t1">员工数量</text>
					<text class="t2">2000</text>
				</view>
				<view class="box column ml">
					<text class="t1">经营状态</text>
					<text class="color1">存续</text>
					<text class="t1">国别/地区</text>
					<text class="t2">印度</text>
					<text class="t1">国家风险评级</text>
					<view class="risk row verCenter">
						<text class="num row rowCenter verCenter">8</text>
						<text class="tt">高风险</text>
						<text class="iconfont icontishi"></text>
					</view>
					<text class="t1">国家主权信用风险评级</text>
					<view class="risk row verCenter">
						<text class="num row rowCenter verCenter">C</text>
						<text class="tt">高风险</text>
						<text class="iconfont icontishi"></text>
					</view>
				</view>
			</view>
			<view class="bar column">
				<text class="t1">经营地址</text>
				<text class="t2">C-7/227, Second Floor Sector-7, Rohini Delhi DL 110085 IN,India</text>
				<text class="t1">注册地址</text>
				<text class="t2">C-7/227, Second Floor Sector-7, Rohini Delhi DL 110085 IN,India</text>
				<text class="t1">主营业务</text>
				<text class="t2">手机批发(SIC：12345678)；手机零售(SIC：87654321)</text>
			</view>
			<view class="risk-error">
				<view class="tit">风险提示</view>
				<view class="list">
					<view class="box row verCenter">
						<view class="num row rowCenter verCenter">1</view>
						<view class="txt">
							企业状态：
							<text class="t1">非存续</text>
							，高危提示！
						</view>
					</view>
					<view class="box row verCenter">
						<view class="num row rowCenter verCenter">2</view>
						<view class="txt">
							国别风险：
							<text class="t2">8</text>
							政治和经济形势不稳定，商业环境不太好，国家风险水平较高。
						</view>
					</view>
					<view class="box row verCenter">
						<view class="num row rowCenter verCenter">3</view>
						<view class="txt">
							国家主权风险：
							<text class="t2">C</text>
							主权债务规模最高，主权债务可持续性最差，主权信用风险水平最高。
						</view>
					</view>
					<view class="box row verCenter">
						<view class="num row rowCenter verCenter">4</view>
						<view class="txt">员工数量：为3，慎防空壳公司。</view>
					</view>
				</view>
			</view>
		</view>
		<!-- 经营信息 -->
		<view class="title row rowCenter verCenter" style="width: 145rpx;">经营信息</view>
		<template v-if="type == 1">
			<view class="business-information">
				<navigator url="/pages/user/buy" hover-class="none">
					<image src="../../static/fj.png" mode="aspectFill" class="business-bggg"></image>
				</navigator>
				<view class="table">
					<view class="box row">
						<view class="left row rowCenter verCenter">财务日期</view>
						<view class="right row rowCenter verCenter">2009年3月27日 — 2020年12月27日</view>
					</view>
					<view class="box row">
						<view class="left row rowCenter verCenter">营业收入</view>
						<view class="right row rowCenter verCenter">$45,458.00（微型企业）</view>
					</view>
					<view class="box row">
						<view class="left row rowCenter verCenter">是否进口商</view>
						<view class="right row rowCenter verCenter">是</view>
					</view>
					<view class="box row">
						<view class="left row rowCenter verCenter">风险诉讼记录</view>
						<view class="right row rowCenter verCenter">12</view>
					</view>
					<view class="box row">
						<view class="left row rowCenter verCenter">累计利润</view>
						<view class="right row rowCenter verCenter">1212</view>
					</view>
					<view class="box row">
						<view class="left row rowCenter verCenter">当年净利润</view>
						<view class="right xf row rowCenter verCenter"></view>
					</view>
				</view>
				<view class="risk-error">
					<view class="tit">风险提示</view>
					<view class="list">
						<view class="box row verCenter">
							<view class="num row rowCenter verCenter">1</view>
							<view class="txt">
								<text>该企业无披露财务数据，注意企业兑付能力与采购能力。点击使用 </text>
								<text @click="toUrl()" class="link" hover-class="none">企业信用报告</text> 
								<text>获取更多内容。</text>
							</view>
						</view>
						<view class="box row verCenter">
							<view class="num row rowCenter verCenter">2</view>
							<view class="txt">该企业为小（微）企业，注意企业兑付能力与采购能力</view>
						</view>
					</view>
				</view>
			</view>
		</template>
		<template v-else-if="type == 2">
			<view class="business-information-sb">
				<view class="business-information-bg">
					<navigator class="bg" url="/pages/user/login" hover-class="none" style="top: 33rpx;right: 33rpx;"></navigator>
				</view>
			</view>
		</template>
		<!-- 关联企业（47关联企业） -->
		<view class="title row rowCenter verCenter" style="width: 290rpx;">关联企业（47关联企业）</view>
		<view v-if="type == 2">
			<view class="relation-sb">
				<view class="relation-bg">
					<navigator class="bg" style="top: 31rpx;right: 37rpx;" url="/pages/user/login" hover-class="none" ></navigator>
				</view>
			</view>
		</view>
		<view class="relation" v-if="type == 1">
			<view class="wrap">
				<view class="bar row">
					<text class="t1">母公司名称</text>
					<text class="t2">Rohini Delhi DL 110085 IN,Indiai DL 110085i DL 110</text>
				</view>
				<view class="bar row">
					<text class="t1">母公司地址</text>
					<text class="t2">C-7/227, Second Floor Sector-7, Rohini Delhi DL 110085 IN,India</text>
				</view>
			</view>
		</view>
		<!-- 管理层（2管理层） -->
		<view class="title row rowCenter verCenter" style="width: 235rpx;">管理层（2管理层）</view>
		<template v-if="type == 2">
			<view class="management-sb">
				<view class="management-bg">
					<navigator class="bg" style="top: 35rpx;right: 37rpx;"  url="/pages/user/login" hover-class="none"></navigator>
				</view>
			</view>
		</template>
		<template v-if="type == 1">
			<view class="management ">
				<view class="wrap">
					<view class="box1 row box">
						<text class="t1 row verCenter">全名</text>
						<text class="t2 row verCenter">Rohini Delhi DL 110085 IN,India</text>
					</view>
					<view class="box2 row box">
						<text class="t1 row verCenter">性别</text>
						<text class="t2 row verCenter">Male</text>
						<text class="t1 row verCenter">岗位</text>
						<text class="t2 row verCenter">President</text>
					</view>
				</view>
				<view class="wrap">
					<view class="box1 row box">
						<text class="t1 row verCenter">全名</text>
						<text class="t2 row verCenter">Rohini Delhi DL 110085 IN,India</text>
					</view>
					<view class="box2 row box">
						<text class="t1 row verCenter">性别</text>
						<text class="t2 row verCenter">Male</text>
						<text class="t1 row verCenter">岗位</text>
						<text class="t2 row verCenter">President</text>
					</view>
				</view>
			</view>
		</template>
		<navigator class="statement" url="/pages/user/agreement" hover-class="none">
			<text class="iconfont iconjinggao"></text>
			<text class="t1">《免责声明》</text>
		</navigator>
		<!-- 更多维度 -->
		<view class="title row rowCenter verCenter" style="width: 143rpx;">更多维度</view>
		<navigator class="more" url="/pages/user/buy" hover-class="none">
			<view class="t1">
				使用
				<text>企业信用报告</text>
				获取更多信息。
			</view>
			<image src="../../static/p3.png" mode="aspectFill" class="im"></image>
		</navigator>
		<view class="login-bar row verCenter" @click="register()" v-if="type == 2">
			<view class="btn row verCenter rowCenter">注册 / 登录</view>
			<text class="txt">免费注册获取更多企业信息。</text>
		</view>
	</view>
</template>

<script>
	import {
		API
	} from '@/util/api.js';

	export default {
		data() {
			return {
				type: 1
			};
		},
		onLoad(options) {
			this.type = options.type;
		},
		onShow() {},
		methods: {
			toUrl(){
				uni.navigateTo({
					url:"/pages/user/buy"
				})
			},
			register() {
				uni.showModal({
					title: '',
					content: '绑定账号，立享更多会员权益！',
					cancelText: '放弃',
					confirmText: '免费注册',
					confirmColor: '#0088DD',
					cancelColor: '#999999',
					success: function(res) {
						if (res.confirm) {
							uni.navigateTo({
								url: '/pages/user/login'
							})
						} else if (res.cancel) {
							console.log('用户点击取消');
						}
					}
				});
			},
			wxLogin() {
				uni.login({
					provider: 'weixin',
					success: loginRes => {
						// 获取用户信息
						uni.getUserInfo({
							provider: 'weixin',
							success: infoRes => {
								uni.showToast({
									title: '授权成功'
								});
							},
							fail: () => {
								uni.showToast({
									title: '授权失败',
									icon: 'none'
								});
							}
						});
					},
					fail: () => {
						uni.showToast({
							title: '授权失败',
							icon: 'none'
						});
					}
				});
			}
		}
	};

</script>

<style scoped lang="scss">
	@import '../../assets/css/detail/index.scss';

</style>
