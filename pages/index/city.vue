<template>
	<view>
		<city-select @cityClick="cityClick" :formatName="formatName" :activeCity="activeCity" :hotCity="hotCity" :obtainCitys="obtainCitys"
		 :isSearch="true" ref="citys"></city-select>
	</view>
</template>

<script>
	import citySelect from '@/components/city-select/city-select.vue';
	export default {
		data() {
			return {
				from: "",
				formatName: 'title',
				activeCity: {
					id: 1,
					title: '中国'
				},
				hotCity: [{
						id: 0,
						title: '美国'
					},
					{
						id: 1,
						title: '香港'
					}
				],
				obtainCitys: [{
						id: 0,
						title: '香港 HKG'
					},
					{
						id: 1,
						title: '美国 USA'
					},
					{
						id: 2,
						title: '中国 CHN'
					}
				]
			};
		},
		onLoad(options) {
			this.from = options.from;
		},
		methods: {
			cityClick(item) {
				console.log(JSON.stringify(item));
				uni.setStorageSync('city', item.title);

				if (this.from == 'search') {
					uni.navigateTo({
						url: '/pages/search/index'
					})
				} else {
					uni.switchTab({
						url: '/pages/index/index'
					});
				}


			}
		},
		components: {
			citySelect
		}
	};

</script>

<style scoped lang="scss"></style>
