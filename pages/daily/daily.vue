<template>
	<view class="container">
		<!-- 日历 -->
		<view class="date-group">
			<view class="date-item" v-for="(item,index) in day_data" :key="index" :style="{ backgroundColor: isToday(item) ? today_color : ''}">
				<text class="week-item" :style="{ color: isToday(item) ? today_week_color : ''}">{{item.weekday}}</text>
				<text class="date-data" :style="{ color: isToday(item) ? today_week_color : ''}">{{item.date}}</text>
			</view>
		</view>
		
		<!-- 任务 -->
		<text class="title">饮食</text>
		<view class="box">
			<image src="../../static/images/早餐.png"></image>
			<view class="food">
				<text class="food-title">早餐</text>
				<text class="food-text">煎蛋，包子，豆浆……</text>
			</view>
			<text class="iconfont-arrow iconfont">&#xe79a</text>
		</view  class="box">
		<view  class="box">
			<image src="../../static/images/中餐.png"></image>
			<view class="food">
				<text class="food-title">中餐</text>
				<text class="food-text">煎蛋，包子，豆浆……</text>
			</view>
			<text class="iconfont-arrow iconfont">&#xe79a</text>
		</view>
		<view  class="box">
			<image src="../../static/images/晚餐.png"></image>
			<view class="food">
				<text class="food-title">晚餐</text>
				<text class="food-text">煎蛋，包子，豆浆……</text>
			</view>
			<text class="iconfont-arrow iconfont">&#xe79a</text>
		</view>
		
	<text class="title">运动</text>
		<view class="box">
			<image src="../../static/images/跑步.png"></image>
			<view class="food">
				<text class="food-title">运动</text>
				<text class="food-text">跑步，跳绳，打羽毛球……</text>
			</view>
			<text class="iconfont-arrow iconfont">&#xe79a</text>
		</view>
	</view>
	
	
</template>

<script setup>
	import { ref,onMounted } from 'vue'
	const day_data = ref([
		{ weekday: '周一', date: 1 },
		{ weekday: '周二', date: 2 },
		{ weekday: '周三', date: 3 },
		{ weekday: '周四', date: 4 },
		{ weekday: '周五', date: 5 },
		{ weekday: '周六', date: 6 },
		{ weekday: '周日', date: 7 }
	])
	
	const today_color = '#e2f3c6'
	const today_week_color = '#4caf50'
	
	// 获取这周的日期,给到day_data
	const getWeekDay = () => {
		const date = new Date()
		const now = date.getDay()
		const week = []
		for (let i = 0; i < 7; i++) {
			const date = new Date()
			date.setDate(date.getDate() - now + i)
			week.push({
				weekday: ['周日', '周一', '周二', '周三', '周四', '周五', '周六'][date.getDay()],
				date: date.getDate()
			})
		}
		day_data.value = week
		
	}
	getWeekDay()
	
	const isToday = (date) => {
		const today = new Date()
		return today.getDate()===date.date
	}
	
	
</script>


<style lang="scss">
	.container {
		padding: 20rpx;
		font-family: 'STSong';
		font-weight: bold;
	}
	
	// .iconfont {
	// 	font-size: 100rpx;
	// 	color: #ffff7f;
	// }
	
	image {
		width: 120rpx;
		height: 120rpx;
	}
	
	.iconfont-arrow {
		font-size: 40rpx;
		color: #57c95b;
	}
	
	.title {
		font-size: 40rpx;
		color: #2d692f;
		margin-left: 30rpx;
	}
	
	.box{
		display: flex;
		align-items: center;
		padding: 35rpx;
		justify-content: space-between;
		border-radius: 40rpx;
		background-color: #ededed;
		margin-top: 40rpx;
		margin-bottom: 40rpx;
		// background-color: #4caf50;
		.food{
			margin-left: 20rpx;
			flex: 1;
			display: flex;
			flex-direction: column;
			justify-content: center;
		}
		.food-title {
			font-size: 36rpx;
			color: #333;
			margin-bottom: 10rpx;
		}
		
		.food-text {
			font-size: 32rpx;
			color: #666;
		}
	}
	
	.date-group {
		display: flex;
		justify-content: space-between;
		margin-bottom: 40rpx;
	}
	
	.date-item {
		display: flex;
		flex-direction: column;
		align-items: center;
		justify-content: center;
		width: 100rpx;
		height: 120rpx;
		border-radius: 20rpx;
	}
	
	.week-item {
		font-size: 32rpx;
		color: #333;
		margin-bottom: 20rpx;
	}
	
	.date-data {
		font-size: 32rpx;
		color: #666;
	}
</style>


