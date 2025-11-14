<template>
	<view class="container">
		<view class="item-box"><text>姓名</text><text>猫猫头</text></view>
		<view class="item-box"><text>性别</text><text>男</text></view>
		<view class="item-box"><text>出生日期</text><text>2000-03-14</text></view>
		<view class="item-box"><text>身高</text><text>175cm</text></view>
		<view class="item-box"><text>体重</text><text>69kg</text></view>
		<view class="item-box"><text>体脂率</text><text>20%</text></view>
		<view class="item-box"><text>血糖</text><text>5.6mmol/L</text></view>
		<view class="item-box"><text>血压</text><text>120/80mmHg</text></view>
		<view class="item-box"><text>心率</text><text>60次/分</text></view>
		<view class="item-box"><text>地址</text><text>四川省成都市</text></view>
		<view class="item-box"><text>电话</text><text>13888888888</text></view>
		<view class="item-box"><text>邮箱</text><text>666666@qq.com</text></view>
		<view class="item-box img-box">
			<uni-section title="选择最近照片" type="line">
				<view class="example-body">
					<uni-file-picker limit="9"></uni-file-picker>
				</view>
			</uni-section>
		</view>
		<view class="item-box"><text>备注</text><text>这是备注</text></view>
		
		<view class="button-box">
			<uni-button type="default" size="default">取消</uni-button>
			<uni-button type="primary" size="default">保存</uni-button>
		</view>

	</view>
</template>

<script setup>
import {
	onMounted,
	reactive,
	ref,
} from "vue"

</script>

<style lang="scss">
.container {
	display: flex;
	flex-direction: column;
	padding: 20px;
	.item-box {
		display: flex;
		justify-content: space-between;
		margin-bottom: 20px;
		font-size: 16px;
		border-bottom: 1px solid #f0f0f0;
		padding-bottom: 10px;
	}
}
.img-box {
	display: flex;
	flex-direction: column;
	.example-body {
		display: flex;
	}
}

.button-box {
	display: flex;
	justify-content: center;
	margin-top: 20px;
	uni-button {
		margin: 0 10px;
	}
}
</style>