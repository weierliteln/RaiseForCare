<template>
	<view class="my-container">
		<!-- 用户信息头部 -->
		<view class="header-section">
			<navigator url="/subpkg/information/information">
				<view class="user-header">
					<view class="user-info">
						<image class="avatar" mode="aspectFill" src="https://img.yzcdn.cn/vant/cat.jpeg" />
						<view class="user-detail">
							<text class="nickname">猫猫头</text>
							<view class="follow-info">
								<text>男</text>
								<text class="separator">|</text>
								<text>183********</text>
							</view>
							
						</view>
						<text class="icon-youbian iconfont icon-arrrow"></text>
					</view>
					
				</view>
			</navigator>
		</view>
		
		<!-- 功能模块 -->
		<view class="function-module">
			<view class="grid-container">
				<block v-for="(item, index) in functionList" :key="index">
					<navigator url="/subpkg/records/records" class="grid-item">
						<view class="grid-item">
							<view class="icon-wrapper" :style="{color:item.colorClass}">
								<text :class="'iconfont ' + item.icon"></text>
							</view>
							<text class="title">{{item.title}}</text>
						</view>
					</navigator>
				</block>
			</view>
		</view>
		
		<!-- 其他设置 -->
		<!-- <view class="other-settings">
			<navigator url="/pages/login/login">登录</navigator>
		</view> -->
	</view>
</template>


<script setup>
	import {
		ref
	} from 'vue';
	const functionList = ref([{
			title: '饮食记录',
			icon: 'icon-icon4',
			colorClass: '#ffd12a'
		},
		{
			title: '血糖记录',
			icon: 'icon-shouye6',
			colorClass: '#f187a9'
		},
		{
			title: '运动记录',
			icon: 'icon-shouye4',
			colorClass: '#56f94a'
		},
		{
			title: '体重记录',
			icon: 'icon-icon7',
			colorClass: '#7cb9f2'
		},
		{
			title: '血压记录',
			icon: 'icon-shouye3',
			colorClass: '#ff6969'
		},
		{
			title: '健康档案',
			icon: 'icon-shouye5',
			colorClass: '#9055A2'
		},
		{
			title: '意见反馈',
			icon: 'icon-shouye7',
			colorClass: '#3C3530'
		}
	])
</script>
<style>
	.my-container {
		min-height: 100vh;
		background-color: #f7f8fa;
	}
	
	.iconfont {
		font-size: 50rpx;
	}
	
	.icon-arrrow {
		font-size: 40rpx;
		color: #666;
		margin-left: auto;
	}

	.my-container .user-header {
		background-color: transparent;
		margin: 0 24rpx;
		border-radius: 24rpx;
		padding: 40rpx;
	}

	.my-container .user-header .user-info {
		display: flex;
		align-items: center;
	}

	.my-container .user-header .user-info .user-detail {
		margin-left: 40rpx;
	}

	.my-container .user-header .user-info .user-detail .nickname {
		font-size: 36rpx;
		font-weight: bold;
		color: #333;
	}

	.my-container .user-header .user-info .user-detail .follow-info {
		margin-top: 16rpx;
		font-size: 14px;
		color: #333;
	}

	.my-container .user-header .user-info .user-detail .follow-info .separator {
		margin: 0 20rpx;
		color: #333;
	}

	.my-container .function-module {
		margin-top: 12px;
		background-color: #fff;
		padding: 20px;
	}

	.function-module .grid-container {
		display: grid;
		justify-content: center;
		grid-template-columns: repeat(4, 1fr);
	}

	.function-module .grid-item {
		display: flex;
		flex-direction: column;
		align-items: center;
		justify-content: center;
		margin-bottom: 20rpx;
	}

	.function-module .icon-wrapper {
		width: 48px;
		height: 48px;
		/* background-color: #f5f6fa; */
		border-radius: 12px;
		display: flex;
		align-items: center;
		justify-content: center;
		margin-bottom: 8px;
	}

	.function-module .title {
		font-size: 14px;
		color: #333;
	}

	.my-container .other-settings {
		margin-top: 12px;
	}

	.my-container .user-header .user-info .avatar {
		width: 80px;
		height: 80px;
		border-radius: 50%;
	}

	/* 添加顶部渐变背景 */
	.header-section {
		background: linear-gradient(to right, #a8dba8, #79bd9a);
		/* background-image: linear-gradient(120deg, #84fab0 0%, #8fd3f4 100%); */
		border-radius: 12px;
		margin: 12px;
		padding-bottom: 20px;
	}

	/* 修改用户信息区域样式，移除背景色使渐变透出 */
	.user-header {
		background-color: transparent;
		margin: 0 12px;
		border-radius: 12px;
		padding: 20px;
	}

	/* 修改用户信息文字颜色 */
	.user-header .user-info .user-detail .nickname {
		font-size: 18px;
		font-weight: bold;
		color: #fff;
	}

	.user-header .user-info .user-detail .follow-info {
		color: rgba(255, 255, 255, 0.8);
	}

	.stats-item .number {
		color: #fff;
	}

	.stats-item .label {
		color: rgba(255, 255, 255, 0.8);
	}

	/* 分隔符颜色调整 */
	.user-header .user-info .user-detail .follow-info .separator {
		color: rgba(255, 255, 255, 0.3);
	}

	/* 图标背景色 */
	.function-module .icon-wrapper.bg-blue {
		background-color: #4080ff;
	}

	.function-module .icon-wrapper.bg-green {
		background-color: #42b883;
	}

	.function-module .icon-wrapper.bg-orange {
		background-color: #ff6b35;
	}

	.function-module .icon-wrapper.bg-purple {
		background-color: #8a2be2;
	}

	/* 修改功能模块样式 */
	.function-module {
		margin: -10px 12px 12px;
		/* 使用负边距让功能模块略微往上 */
		background-color: #fff;
		padding: 20px;
		border-radius: 12px;
	}
</style>