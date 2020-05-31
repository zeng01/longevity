<template>
	<view  class="category">
		<view class="tab">
			<scroll-view :scroll-top="scrollTop" scroll-y="true" class="scroll-y" show-scrollbar='false'>
				<view class="tab_list" :class="{'active':is_tab==item.id}" v-for="item in tab_list" :key="item.id">全部商品</view>
			</scroll-view>
		</view>
		<view class="content">
			<view class="content_tab">
				<view class='tab_list' :class="{'active':is_sort==0}">销量</view>
				<view class='tab_list' :class="{'active':is_sort==1}">价格</view>
			</view>
			<view class="product">
				<scroll-view :scroll-top="scrollTop" scroll-y="true" show-scrollbar='false' class="scroll-y product_scroll">
					<view class="product_list" v-for="item in product_list" :key="item.id">
						<image :src="item.pic" mode=""></image>
						<view class="title">{{item.title}}</view>
					</view>
				</scroll-view>
			</view>
		</view>
	</view>
</template>

<script>
	import imgUrl from '@/static/img/logo.png'
	export default {
		data() {
			return {
				is_tab:1,
				is_sort:0,
				scrollTop:0,
				tab_list:[
					{id:1,title:'全部商品'},
					{id:2,title:'全部商品'},
					{id:3,title:'全部商品'},
					{id:4,title:'全部商品'},
					{id:5,title:'全部商品'},
					{id:6,title:'全部商品'},
					{id:7,title:'全部商品'},
					{id:8,title:'全部商品'},
					{id:9,title:'全部商品'},
					{id:10,title:'全部商品'},
					{id:11,title:'全部商品'},
					{id:12,title:'全部商品'},
					{id:13,title:'全部商品'},
					{id:14,title:'全部商品'},
					{id:15,title:'全部商品'},
					{id:16,title:'全部商品'},
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
			}
		},
		methods: {
			
		}
	}
</script>

<style scoped>
.category{
	display: flex;
}

.tab{
	background: #ccc;
	height: 100%;
}

.scroll-y{
	height: 500px;
}

.tab_list{
	text-align: center;
	padding: 30rpx 20rpx;
}

.tab .active{
	background-color: #fff;
}

.content{
	flex: 1;
	height: 100%;
	display: flex;
	flex-direction: column;
}

.content_tab{
	display: flex;
}

.tab_list{
	flex: 1;
	text-align: center;
	padding: 30rpx 20rpx;
	border-bottom: 1px solid #ccc;
}

.content_tab .active{
	color: #007AFF;
}

.product{
	flex: 1;
}

.product_list{
	padding: 20rpx;
	width: 50%;
	float:left;
	box-sizing: border-box;
}

.product_list image{
	width: 100%;
	margin-bottom: 10rpx;
}
</style>
