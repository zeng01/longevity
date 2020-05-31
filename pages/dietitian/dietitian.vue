<template>
	<view class="bg_color">
		<view class="search">
			<text>搜索营养师</text>
		</view>
		<view class="dietitian">
			<view class="dietitian_list">
				<image src="../../static/img/logo.png" mode=""></image>
				<view class="dietitian_info">
					<view class="name">
						<text>王静美</text>
						<text>5</text>
					</view>
					<view>专业方向：营养健康，预防疾病</view>
					<view>资质年限：10年</view>
					<view>所属店铺：生命波营养液体验中心（哈尔滨龙山路口）</view>
				</view>
				<view class="submit">所属服务</view>
			</view>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				
			}
		},
		methods: {
			
		}
	}
</script>

<style scoped>
.bg_color{
	background-color: #f3f4f5;
	height: 100%;
}
	
.search{
	text-align: center;
	background-color: #ccc;
	padding: 30rpx 0;
	margin: 20rpx;
}

.dietitian_list{
	display: flex;
	align-items: center;
	padding: 30rpx 20rpx;
	background-color: #fff;
}

.dietitian_list image{
	width: 80rpx;
	height: 80rpx;
}

.dietitian_info{
	flex: 1;
	margin: 0 20rpx;
	font-size: 24rpx;
}

.dietitian_info .name{
	font-size: 28rpx;
	font-weight: 700;
}

.submit{
	height: 60rpx;
	line-height: 60rpx;
	padding: 0 40rpx;
	background-color: #007AFF;
	color: #fff;
	border-radius: 60rpx;
}
</style>
