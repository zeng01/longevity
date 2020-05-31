<template>
	<view class="content">
		<view class="uni-padding-wrap">
			<view class="page-section swiper">
				<view class="page-section-spacing">
					<swiper class="swiper" :indicator-dots="indicatorDots" :autoplay="autoplay" :interval="interval" :duration="duration" circular='true'>
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
		<view class="hot_shop">
			<view class="hot" v-for="item in hot_list" :key="item.id">
				<view class="hot_title">
					{{item.title}}
				</view>
				<view class="hot_img">
					<image :src="itemPic" v-for="(itemPic,index) in item.pic " :key="index" mode=""></image>
				</view>
			</view>
		</view>
		<view class="product">
			<view class="product_title">
				<text>热门推荐</text>
				<text class="find">发现美好生活</text>
			</view>
			<view class="product_list">
				<view class="product_hasList" v-for="(item,index) in product_list" :key="index">
					<image :src="item.pic" mode=""></image>
					<view class="title">{{item.title}}</view>
					<view class="product_price">
						<text class="price">￥{{item.price}}</text>
						<text class="num">{{item.num}}人购买</text>
					</view>
				</view>
			</view>
		</view>
	</view>
</template>

<script>
	import page_hot from '../../components/hot'
	import imgUrl from '@/static/img/logo.png'
	export default {
		components:{
			page_hot
		},
		data() {
			return {
				indicatorDots: true,
				autoplay: true,
				interval: 5000,
				duration: 500,
				hot_list:[
					{title:'热卖',pic:[imgUrl,imgUrl]},
					{title:'金牌商店',pic:[imgUrl,imgUrl]},
				],
				product_list:[
					{id:1,pic:imgUrl,title:'人参根饮液',price:345,num:456},
					{id:2,pic:imgUrl,title:'人参根饮液',price:345,num:456},
					{id:3,pic:imgUrl,title:'人参根饮液',price:345,num:456},
					{id:4,pic:imgUrl,title:'人参根饮液',price:345,num:456},
					{id:5,pic:imgUrl,title:'人参根饮液',price:345,num:456},
					{id:6,pic:imgUrl,title:'人参根饮液',price:345,num:456},
					{id:7,pic:imgUrl,title:'人参根饮液',price:345,num:456},
					{id:8,pic:imgUrl,title:'人参根饮液',price:345,num:456},
					{id:9,pic:imgUrl,title:'人参根饮液',price:345,num:456},
					{id:10,pic:imgUrl,title:'人参根饮液',price:345,num:456},
				]
			};
		}
	}
</script>

<style>
	.swiper-item {
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

	.nav {
		display: flex;
		flex-wrap: wrap;
		padding: 20rpx 0;
		background-color: #fff;
	}
	
	.nav_list {
		width: 25%;
		text-align: center;
		font-size: 28rpx;
		margin: 20rpx 0;
	}
	
	.nav_list .nav_img{
		width: 60rpx;
		height: 60rpx;
	}
	
	.hot_shop{
		display: flex;
		margin: 40rpx 20rpx;
		height: 240rpx;
	}
	
	.hot_shop_list{
		width: 48%;
		height: 240rpx;
	}
	
	.hot_shop_list:first-child{
		margin-right: 24rpx;
	}
	.hot {
		padding: 20rpx;
		background-color: #fff;
		height: 100%;
		width: 48%;
		box-sizing: border-box;
	}
	
	.hot_title {
		margin: 10rpx 0;
	}
	
	.hot_img {
		display: flex;
		height: 70%;
	}
	
	.hot_img image {
		flex: 1;
		height: 100%;
	}
	
	.hot_img image:first-child {
		margin-right: 20rpx;
	}
	
	.hot:first-child{
		margin-right: 24rpx;
	}
	
	.product{
		margin: 20rpx;
	}
	
	.product_title{
		margin-bottom:20rpx ;
	}
	
	.product_title .find{
		margin: 0 20rpx;
		padding: 10rpx 20rpx;
		background-color: #007AFF;
		color: #fff;
		border-radius: 40rpx;
		font-size: 24rpx; 
	}
	
	.product_list .product_hasList{
		float: left;
		width: 48%;
		padding: 14rpx;
		background-color: #fff;
		box-sizing: border-box;
		margin: 0 8rpx;
	}
	
	.product_hasList image{
		width: 100%;
		max-height: 300rpx;
	}
	
	.product_hasList .title{
		margin: 10rpx 0;
	}
	.product_price .price{
		color: #007AFF;
	}
	
	.product_price .num{
		margin: 0 14rpx;
		color: #999;
		font-size: 24rpx;
	}
</style>
