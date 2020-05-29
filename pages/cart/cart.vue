<template>

	<view class="content">
		<view class="uni-padding-wrap">
			<view class="page-section swiper">
				<view class="page-section-spacing">
					<swiper class="swiper" :indicator-dots="indicatorDots" :autoplay="autoplay" :interval="interval" :duration="duration">
						<swiper-item>
							<view class="swiper-item uni-bg-red">A</view>
						</swiper-item>
						<swiper-item>
							<view class="swiper-item uni-bg-green">B</view>
						</swiper-item>
						<swiper-item>
							<view class="swiper-item uni-bg-blue">C</view>
						</swiper-item>
					</swiper>
				</view>
			</view>
		</view>
		
		            <view class="nav">
		                <navigator url="/components/notice/notice" hover-class="navigator-hover" class="nav_list">
		                    <image class="nav_img" src="/static/img/logo.png"></image>
							<view class="nav_text">通知公告</view>
		                </navigator>
		                <navigator url="" hover-class="navigator-hover" class="nav_list">
		                    <image class="nav_img" src="/static/img/logo.png"></image>
		                	<view class="nav_text">通知公告</view>
		                </navigator>
						<navigator url="" hover-class="navigator-hover" class="nav_list">
						    <image class="nav_img" src="/static/img/logo.png"></image>
							<view class="nav_text">通知公告</view>
						</navigator>
						<navigator url="" hover-class="navigator-hover" class="nav_list">
						    <image class="nav_img" src="/static/img/logo.png"></image>
							<view class="nav_text">通知公告</view>
						</navigator>
						<navigator url="" hover-class="navigator-hover" class="nav_list">
						    <image class="nav_img" src="/static/img/logo.png"></image>
							<view class="nav_text">通知公告</view>
						</navigator>
						<navigator url="" hover-class="navigator-hover" class="nav_list">
						    <image class="nav_img" src="/static/img/logo.png"></image>
							<view class="nav_text">通知公告</view>
						</navigator>
						<navigator url="" hover-class="navigator-hover" class="nav_list">
						    <image class="nav_img" src="/static/img/logo.png"></image>
							<view class="nav_text">通知公告</view>
						</navigator>
						<navigator url="" hover-class="navigator-hover" class="nav_list">
						    <image class="nav_img" src="/static/img/logo.png"></image>
							<view class="nav_text">通知公告</view>
						</navigator>
		            </view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				title: 'Hello',
				indicatorDots: true,
				autoplay: true,
				interval: 2000,
				duration: 500
			}
		},
		onLoad() {

		},
		methods: {

		}
	}
</script>

<style>
	.content {}
	.swiper-item{
		height: 100%;
	}
	.uni-bg-green {
		background: #4CD964;
	}

	.uni-bg-blue {
		background: #098;
	}

	.uni-bg-red {
		background: #f34;
	}
	
	.nav{
		display: flex;
		flex-wrap: wrap;
	}
	

	
</style>
