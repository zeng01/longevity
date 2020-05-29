<template>
	<view class="hot_bg">
		<view class="hot" v-for="item in hot_list" :key="item.id">
			<view class="hot_title">
				{{item.title}}
			</view>
			<view class="hot_img">
				<image :src="itemPic" v-for="itemPic in item.pic " mode=""></image>
			</view>
		</view>
	</view>
</template>

<script>
 export default {
  name: "page-notes",
  props: {
    hot_list: {
    type: Array,
    default: ()=>[]
   }
  },
	data(){
		return {
			list:[],
			isTop:false
		}
	},
  created() {
    // this.activeNotes()
  },
  methods: {
    
  }
 }
</script>

<style>
	.hot_bg{
		height: 240rpx;
		display: flex;
		margin: 40rpx 20rpx;
	}
	.hot {
		padding: 20rpx;
		background-color: #fff;
		height: 100%;
		width: 45%;
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
</style>
