<script>
	export default {
		onLaunch: function() {
			console.log('App Launch')
		},
		onShow: function() {
			console.log('App Show')
		},
		onHide: function() {
			console.log('App Hide')
		}
	}
</script>

<style>
	/*每个页面公共css */
	*{
		padding: 0;
		margin: 0;
		box-sizing: border-box;
	}
	
	body{
		background-color: #f5f5f5;
		font-size: 28rpx;
	}
</style>
