<template>
	<view class="history-index">
		<view class="h-head row verCenter">
			<view class="search-box row bothSide">
				<view class="search-bar row verCenter">
					<view class="country row verCenter" @click="choice()">
						<text class="arrow"></text>
						<text class="txt">{{city}}</text>
					</view>
					<input type="text" class="inp" :value="name" placeholder="请输入企业名称关键词" placeholder-style="color:#999999;" />
				</view>
				<view class="btn row rowCenter verCenter">查一下</view>
			</view>
		</view>
		<view class="list">
			<navigator class="box" url="/pages/detail/index?type=1" hover-class="none">
				<text class="t1">LAVA INTERNATIONAL LIMITED INTERNATIONINTERNATIONINTERNATION</text>
				<view class="row verCenter">
					<text class="color1">非存续</text>
					<text class="line"></text>
					<text class="tt">印度 IND</text>
				</view>
				<text class="t2">企业经营地址：C-DDS/77,Sshubdbjejjnk Fhjdsj R jsjsj. 1587sj</text>
			</navigator>
			<navigator class="box" url="/pages/detail/index?type=1" hover-class="none">
				<text class="t1">LAVA INTERNATIONAL LIMITED INTERNATIONINTERNATIONINTERNATION</text>
				<view class="row verCenter">
					<text class="color1">非存续</text>
					<text class="line"></text>
					<text class="tt">印度 IND</text>
				</view>
				<text class="t2">企业经营地址：C-DDS/77,Sshubdbjejjnk Fhjdsj R jsjsj. 1587sj</text>
			</navigator>
			<navigator class="box" url="/pages/detail/index?type=1" hover-class="none">
				<text class="t1">LAVA INTERNATIONAL LIMITED INTERNATIONINTERNATIONINTERNATION</text>
				<view class="row verCenter">
					<text class="color2">存续</text>
					<text class="line"></text>
					<text class="tt">印度 IND</text>
				</view>
				<text class="t2">企业经营地址：C-DDS/77,Sshubdbjejjnk Fhjdsj R jsjsj. 1587sj</text>
			</navigator>
			<navigator class="box" url="/pages/detail/index?type=1" hover-class="none">
				<text class="t1">LAVA INTERNATIONAL LIMITED INTERNATIONINTERNATIONINTERNATION</text>
				<view class="row verCenter">
					<text class="color1">非存续</text>
					<text class="line"></text>
					<text class="tt">印度 IND</text>
				</view>
				<text class="t2">企业经营地址：C-DDS/77,Sshubdbjejjnk Fhjdsj R jsjsj. 1587sj</text>
			</navigator>
			<navigator class="box" url="/pages/detail/index?type=1" hover-class="none">
				<text class="t1">LAVA INTERNATIONAL LIMITED INTERNATIONINTERNATIONINTERNATION</text>
				<view class="row verCenter">
					<text class="color1">非存续</text>
					<text class="line"></text>
					<text class="tt">印度 IND</text>
				</view>
				<text class="t2">企业经营地址：C-DDS/77,Sshubdbjejjnk Fhjdsj R jsjsj. 1587sj</text>
			</navigator>
			<navigator class="box" url="/pages/detail/index?type=1" hover-class="none">
				<text class="t1">LAVA INTERNATIONAL LIMITED INTERNATIONINTERNATIONINTERNATION</text>
				<view class="row verCenter">
					<text class="color1">非存续</text>
					<text class="line"></text>
					<text class="tt">印度 IND</text>
				</view>
				<text class="t2">企业经营地址：C-DDS/77,Sshubdbjejjnk Fhjdsj R jsjsj. 1587sj</text>
			</navigator>
			<navigator class="box" url="/pages/detail/index?type=1" hover-class="none">
				<text class="t1">LAVA INTERNATIONAL LIMITED INTERNATIONINTERNATIONINTERNATION</text>
				<view class="row verCenter">
					<text class="color1">非存续</text>
					<text class="line"></text>
					<text class="tt">印度 IND</text>
				</view>
				<text class="t2">企业经营地址：C-DDS/77,Sshubdbjejjnk Fhjdsj R jsjsj. 1587sj</text>
			</navigator>
			<navigator class="box" url="/pages/detail/index?type=1" hover-class="none">
				<text class="t1">LAVA INTERNATIONAL LIMITED INTERNATIONINTERNATIONINTERNATION</text>
				<view class="row verCenter">
					<text class="color1">非存续</text>
					<text class="line"></text>
					<text class="tt">印度 IND</text>
				</view>
				<text class="t2">企业经营地址：C-DDS/77,Sshubdbjejjnk Fhjdsj R jsjsj. 1587sj</text>
			</navigator>
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
				city:'CHN 中国'
			};
		},
		onLoad(options) {
			this.name = options.name || '';
		},
		onShow() {
			var city=uni.getStorageSync('city');
			if(city){
				this.city=city;
			}
		},
		onPullDownRefresh() {
			this.refresh();
		},
		methods: {
			getData() {},
			choice(){
				uni.navigateTo({
					url:'/pages/index/city?from=search'
				})
			},
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
