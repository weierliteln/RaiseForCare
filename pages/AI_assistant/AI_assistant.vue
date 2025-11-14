<template>
	<view class="ai-page">
		<!-- AI头像和介绍 -->
		<view class="message-box">
			<view class="ai-intro">
				<image class="ai-avatar" src="/static/images/机器人.png"  mode="aspectFill"/>
				<view class="ai-message">
					主人，关于您遇到的问题，我都可以帮您解答哦~
				</view>
			</view>
			<view class="my-intro">
				<view class="my-message">
					今天吃什么？
				</view>
				<image class="my-avatar" src="https://img.yzcdn.cn/vant/cat.jpeg" mode="aspectFill" />
			</view>
		</view>

		<!-- 常见问题卡片 -->
		<view class="qa-card">
			<view class="card-title">
				<van-icon name="chat-o" color="#4080ff" size="18px" />
				<text>常见问题</text>
			</view>
			<view class="qa-list">
				<text>早餐吃什么？</text>
				<text>中餐吃什么？糖醋排骨？红烧里脊？...</text>
				<text>晚餐吃什么？糖醋排骨？红烧里脊？...</text>
				<text>夜宵吃什么？糖醋排骨？红烧里脊？...</text>
			</view>
		</view>

		<!-- 底部功能区 -->
		<view class="bottom-section">
			<!-- 快捷功能 -->
			<view class="quick-actions">
				<view class="action-item">
					<text>五分钟了解饮食</text>
				</view>
				<view class="action-item">
					<text>找咨询团队</text>
				</view>
				<view class="action-item">
					<text>如何健身</text>
				</view>
			</view>

			<!-- 输入框区域 -->
			<view class="input-section">
				<view class="input-box">
					<input class="placeholder" placeholder="有问题可以直接向我提哦"></input>
				</view>
				<view class="send-btn">
					<text>发送</text>
				</view>
			</view>
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
	.ai-page {
		min-height: 100vh;
		// background: linear-gradient(180deg, #4bc2f1 0%, #87CEEB 20%, #f7f8fa 100%);
		padding-bottom: 200rpx; // 为底部留出空间
	}

.message-box{
	.ai-intro {
		padding: 30rpx 20px;
		display: flex;
		align-items: flex-start;
		gap: 24rpx;
		
		.ai-avatar {
			display: block;
			width: 80rpx;
			height: 80rpx;
			border-radius: 100%;
		}
		
		.ai-message {
			background: #fff;
			padding: 24rpx 32rpx;
			border-radius: 16rpx;
			border-top-left-radius: 4px;
			font-size: 14px;
			color: #333;
			max-width: 70%;
			align-self: flex-end;
			background-color: #a8dba8;
		}
		
	}
	
	.my-intro {
		padding: 0rpx 40rpx;
		display: flex;
		align-items: flex-start;
		justify-content: flex-end;
		gap: 24rpx;
		
		.my-avatar {
			width: 80rpx;
			height: 80rpx;
			aign-self: flex-end;
			border-radius: 100%;
		}
		
		.my-message {
			background: #fff;
			padding: 24rpx 32rpx;
			border-radius: 16rpx;
			border-top-right-radius: 4px;
			font-size: 14px;
			color: #333;
			max-width: 70%;
			background-color: #79bd9a;
		}
	}
}

	.qa-card {
		margin: 20px 16px;
		background: #fff;
		border-radius: 12px;
		padding: 16px;
		
		.card-title {
			display: flex;
			align-items: center;
			gap: 8px;
			margin-bottom: 12px;
			font-size: 16px;
			font-weight: bold;
		}
		
		.qa-list {
			display: flex;
			flex-direction: column;
			gap: 12px;
			
			text {
				color: #666;
				font-size: 14px;
			}
		}
	}

	.bottom-section {
		position: fixed;
		bottom: 0;
		left: 0;
		right: 0;
		background: #fff;
		padding: 12px 16px;
		
		.quick-actions {
			display: flex;
			justify-content: space-around;
			margin-bottom: 12px;
			
			.action-item {
				color: #666;
				font-size: 14px;
			}
		}
		
		.input-section {
			display: flex;
			align-items: center;
			gap: 12px;
			
			.input-box {
				flex: 1;
				background: #f5f5f5;
				height: 80rpx;
				border-radius: 20px;
				padding: 0 16px;
				display: flex;
				align-items: center;
				
				.placeholder {
					color: #999;
					font-size: 14px;
				}
			}
			
			.send-btn {
				width: 200rpx;
				height: 80rpx;
				background: #f5f5f5;
				border-radius: 20rpx;
				display: flex;
				align-items: center;
				justify-content: center;
			}
		}
	}
</style>
