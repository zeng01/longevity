<template>
<viw class="cart">
	<view class="cart_list">
		<view class="cart_left">
			<text class="select" :class="{'is_select':is_select}"></text>
			<image src="../../static/img/logo.png" mode=""></image>
			<view class="cart_info">
				<view class="title">人参根饮液</view>
				<view class="num">规格：95mlx10瓶</view>
				<view class="price">300.00</view>
			</view>
		</view>
		<view class="cart_op">
			<text @click="getJian">-</text>
			<input type="text" v-model="num" class="number" />
			<text @click="getJia">+</text>
		</view>
	</view>
	<view class="cart_footer">
		<view class="select_all">
			<text class="select" :class="{'is_select':is_select}"></text>
			<text>全选</text>
		</view>
		<view class="submit">去结算</view>
	</view>
</viw>
</template>

<script>
	export default {
		data() {
			return {
				num:0,
				is_select:false,
			}
		},
		onLoad() {

		},
		methods: {
			getJia(){
				this.num++
			},
			getJian(){
				this.num--
			}
		}
	}
</script>

<style scoped>
.cart{
	background-color: #f3f4f5;
}
	
.cart_list{
	display: flex;
	margin: 20rpx 0;
	justify-content: space-between;
	padding: 20rpx ;
	background-color: #fff;
}

.cart_left{
	display: flex;
	align-items: center;
}

.cart_left image{
	max-width: 180rpx;
	margin: 0 20rpx;
	max-height: 180rpx;
}

.cart_info .num{
	margin: 40rpx 0;
	padding: 10rpx 20rpx;
	background: #ccc;
}

.cart_info .price{
	color: #f43;
}

.cart_op{
	flex: 1;
	display: flex;
	justify-content: flex-end;
	align-items: flex-end;
}
	
.cart_footer{
	position: fixed;
	bottom: 0;
	left: 0;
	padding: 30rpx;
	display: flex;
	justify-content: space-between;
}
.select{
	width: 30rpx;
	height: 30rpx;
	border-radius: 50%;
	display: inline-block;
	border:1px solid #333;
	margin-right: 16rpx;
}	

.is_select{
	background-color: #007AFF;
}

.number{
	width: 80rpx;
	height: 30rpx;
	border: 1px solid #333;
	text-align: center;
	margin: 0 20rpx;
}
</style>
