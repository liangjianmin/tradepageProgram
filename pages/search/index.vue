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
			<navigator class="box" url="/pages/detail/index?type=3" hover-class="none">
				<text class="t1">Apple Inc.</text>
				<view class="row verCenter">
					<text class="color1">存续</text>
					<text class="line"></text>
					<text class="tt">美国USA</text>
				</view>
				<text class="t2">企业经营地址：1 Apple Park Way, Cupertino, CA, 95014, UNITED STATES</text>
			</navigator>
			<navigator class="box" url="/pages/detail/index?type=4" hover-class="none">
				<text class="t1">Google LLC</text>
				<view class="row verCenter">
					<text class="color1">存续</text>
					<text class="line"></text>
					<text class="tt">美国USA</text>
				</view>
				<text class="t2">企业经营地址：1600 Amphitheatre Pkwy, Mountain View, CA, 94043, UNITED STATES</text>
			</navigator>
			<navigator class="box" url="/pages/detail/index?type=2" hover-class="none">
				<text class="t1">Sample Company - Before Login</text>
				<view class="row verCenter">
					<text class="color2">存续</text>
					<text class="line"></text>
					<text class="tt">国家CON</text>
				</view>
				<text class="t2">企业经营地址：Address Address Address Address Address</text>
			</navigator>
			<navigator class="box" url="/pages/detail/index?type=1" hover-class="none">
				<text class="t1">Sample Company - After Login</text>
				<view class="row verCenter">
					<text class="color1">非存续</text>
					<text class="line"></text>
					<text class="tt">国家CON</text>
				</view>
				<text class="t2">企业经营地址：Address Address Address Address Address</text>
			</navigator>
			<navigator class="box" url="/pages/detail/index?type=2" hover-class="none">
				<text class="t1">Sample Company - Before Login</text>
				<view class="row verCenter">
					<text class="color2">存续</text>
					<text class="line"></text>
					<text class="tt">国家CON</text>
				</view>
				<text class="t2">企业经营地址：Address Address Address Address Address</text>
			</navigator>
			<navigator class="box" url="/pages/detail/index?type=1" hover-class="none">
				<text class="t1">Sample Company - After Login</text>
				<view class="row verCenter">
					<text class="color1">非存续</text>
					<text class="line"></text>
					<text class="tt">国家CON</text>
				</view>
				<text class="t2">企业经营地址：Address Address Address Address Address</text>
			</navigator>
			<navigator class="box" url="/pages/detail/index?type=2" hover-class="none">
				<text class="t1">Sample Company - Before Login</text>
				<view class="row verCenter">
					<text class="color2">存续</text>
					<text class="line"></text>
					<text class="tt">国家CON</text>
				</view>
				<text class="t2">企业经营地址：Address Address Address Address Address</text>
			</navigator>
			<navigator class="box" url="/pages/detail/index?type=1" hover-class="none">
				<text class="t1">Sample Company - After Login</text>
				<view class="row verCenter">
					<text class="color1">非存续</text>
					<text class="line"></text>
					<text class="tt">国家CON</text>
				</view>
				<text class="t2">企业经营地址：Address Address Address Address Address</text>
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
