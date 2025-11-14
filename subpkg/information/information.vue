<template>
	<view class="container">
		<view class="box">
			<view class="item-box">
				<text>修改头像</text>
				<image class="avatar" mode="aspectFill" src="https://img.yzcdn.cn/vant/cat.jpeg" />
			</view>
			<view class="item-box">
				<text>昵称</text>
				<text>猫猫头</text>
			</view>
			<view class="item-box">
				<text>手机号</text>
				<text>183********</text>
			</view>
			<view class="item-box">
				<text>密码</text>
				<text>****</text>
			</view>
		</view>
		<navigator url="/pages/login/login"><button class="btn">退出登录</button></navigator>
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

<style lang="scss">
	.container {
		// background-color: #f5f5f5;
		height: 100%;
	}

	.box {
		margin-top: 20rpx;
		background-color: #fff;
		padding: 20rpx;
	}

	.item-box {
		display: flex;
		justify-content: space-between;
		align-items: center;
		padding: 20rpx;
		font-size: 18px;
		border-bottom: 1px solid #f5f5f5;
	}

	.avatar {
		width: 80rpx;
		height: 80rpx;
		border-radius: 50%;
	}

	.btn {
		width: 50%;
		margin: 40rpx auto;
		padding: 10rpx;
		background-color: #a8dba8;
		border-radius: 12px;
		color: #333;

	}
</style>