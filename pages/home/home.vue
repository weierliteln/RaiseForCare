<template>
	
	<view class="bg-box">
		<view class="title">
		<text>快开始</text>
		<text>你的健康计划吧！</text>
		</view>
		<!-- <image class="home_bg" src="/static/images/首页背景.jpg" mode="aspectFill"></image> -->
		<image class="home-bg" src="/static/images/运动组.png" mode="aspectFit"></image>
		<!-- <image class="home-bg" src="/static/images/运动女青年3.png" mode="aspectFit"></image> -->
	</view>

	<view class="container">
		<view class="grid">
			<navigator class="grid-item" url="/subpkg/blood_sugar/blood_sugar">
				<view >
					<text class="iconfont" style="color:mediumvioletred;">&#xe636</text>
					记血糖	
					<text style="font-size: 38rpx; margin-top: 26rpx; color: mediumvioletred;">6.2mmol/L</text>
				</view>
			</navigator>
			<navigator class="grid-item" url="/subpkg/blood_pressure/blood_pressure">
				<view>
					<text class="iconfont" style="color:red;">&#xe628</text>
					记血压
					<text style="font-size: 38rpx; margin-top: 26rpx; color: red;">6.2mmol/L</text>
				</view>
				</navigator>
			<navigator class="grid-item" url="/subpkg/sport/sport">
				<view>
					<text class="iconfont" style="color:orange;">&#xe62a</text>
					记运动
					<text>今日消耗</text>
					<text>1189col</text>
				</view>
				</navigator>
			<navigator class="grid-item" url="/subpkg/food/food">
				<view>
					<text class="iconfont" style="color:green;">&#xe66e</text>
					记饮食
					<text>今日摄入</text>
					<text>1298col</text>
				</view>
				</navigator>

			<navigator class="grid-item" url="/subpkg/weight/weight">
				<view>
					<text class="iconfont" style="color:lightseagreen;">&#xe696</text>
					记体重
					<text>69kg</text>
					<text>未达目标</text>
				</view>
				</navigator>
			<!-- <view class="grid-item">
				6
			</view> -->
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {

			};
		}
	}
</script>

<style lang="scss" scoped>
	.bg-box {
		// 字体为圆体
		font-family: 'YouYuan';
		font-weight: 800;	
		width: 100%;
		height: 300rpx;
		display: flex;
		justify-content: space-between;
		align-items: center;
		background-color: #f7f8fa;
		padding: 0 20rpx;
		color: #534847;
		.title {
			display: flex;
			flex-direction: column;
			font-size: 50rpx;
			color: #333;
			margin: 40rpx 40rpx 0 40rpx;
			// color: #2d692f;
			z-index: 100001;
			text{
				white-space: nowrap;
				margin-bottom: 20rpx;
			}
			
		}
		}
		.home-bg {
			// 靠右
			position: absolute;
			// bottom: 0;
			right:0%;
			width: 60%;
			// height: 100%;
			z-index: 10000;
		}

	.iconfont {
		font-size: 45rpx;
		margin-right: 10rpx;
	}

	.container {
		width: 100%;
		height: 100%;
		position: relative;
		// bottom: 40rpx;
		border-radius: 40rpx 40rpx 0 0;
		background-color: #fff;
		padding: 40rpx 0;

		.grid {
			display: grid;
			grid-template-columns: 50% 50%;
			padding: 0 40rpx;
		}

		.grid-item {
			background-color: #f3f3f3;
			border-radius: 40rpx;
			height: 140rpx;
			margin: 20rpx 10rpx;
			padding: 40rpx;
			font-size: 32rpx;
			text:nth-child(2),text:nth-child(3){
				display: block;
				margin-top: 5rpx;
				font-size: 28rpx;
			}
			text:nth-child(2){
				margin-top: 40rpx;
			}
			text:nth-child(3){
				color: #666;
			}
			
		}
	
		.grid-item:nth-child(1) {
			background-color: #ffcfdf;
		}
		.grid-item:nth-child(2) {
			background-color: #ffe2e2;
		}
		.grid-item:nth-child(3) {
			background-color: #e0f9b5;
		}
		.grid-item:nth-child(4) {
			background-color: #fefdca;
		}
		.grid-item:nth-child(5) {
			background-color: #b9d7ea;
		}
		.grid-item:nth-child(6) {
			background-color: #d6e6f2;
			}
	}
</style>