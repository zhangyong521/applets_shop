<template>
	<view class="home">
		<swiper indicator-dots circular 
		autoplay="true" 
		interval="3000" 
		duration="500">
			<swiper-item v-for="item in swipers" :key="item.id">
				<image :src="item.img"></image>
			</swiper-item>
		</swiper>
		
		<!-- 导航区域 -->
		<view class="nav">
			<view class="nav_item" v-for="(item,index) in navs" :key="index" @click="navItemClick(item.path)">
				<view :class="item.icon"></view>
				<text>{{item.title}}</text>
			</view>
		</view>
		
	</view>
</template>

<script>
	export default {
		data() {
			return {
				swipers: [],
				navs: [
					{
						icon: 'iconfont icon-shouye',
						title: '我的超市',
						path: '/pages/goods/goods'
					},
					{
						icon: 'iconfont icon-tuangou',
						title: '联系我们',
						path: '/pages/contact/contact'
					},
					{
						icon: 'iconfont icon-mendianguanli',
						title: '社区图片',
						path: '/pages/pics/pics'
					},
					{
						icon: 'iconfont icon-daishouhuo',
						title: '学习视频',
						path: '/pages/videos/videos'
					}
				]
			}
		},
		onLoad() {
			this.getSwipers()
		},
		methods: {
			// 获取轮播图的数据
			async getSwipers () {
				const res = await this.$myRuquest({
					url: '/api/getlunbo'
				})
				this.swipers = res.data.message
			},
			
			// 导航点击的处理函数
			navItemClick (url) {
				uni.navigateTo({
					url
				})
			}
			
		}
	}
</script>

<style lang="scss">
	.home{
		swiper{
			width: 750rpx;
			height: 380rpx;
			image{
				height: 100%;
				width: 100%;
			}
		}
		.nav {
			display: flex;
			.nav_item {
				width: 25%;
				text-align: center;
				view{
					width: 120rpx;
					height: 120rpx;
					background: $shop-color;
					border-radius: 60rpx;
					margin: 10px auto;
					line-height: 120rpx;
					color: #fff;
					font-size: 50rpx;
				}
				.iconfont {
				   font-size: 70rpx;
				}
				text{
					font-size: 28rpx;
				}
			}
		}
	}
</style>
