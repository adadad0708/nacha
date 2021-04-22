<template>
	<view class="container">
		<view class="header">
			<!-- 搜索栏 begin -->
			<view class="search-box">
				<view class="search-input" @tap="showSearch=true">
					<image src="/static/images/common/search-icon.png" class="search-icon"></image>
					<view>搜索
					</view>
				</view>
			</view>
			<!-- 搜索栏 end -->
			<view class="center">
				<view class="store">
					<view class="title">
						<image :src="orderType == 'takein' ? 
								'/static/images/common/star_normal.png' : 
								'/static/images/order/order_icon_address.png'" 
								class="left-icon" />
						<!-- 为了测试方便，这里使用静态店铺数据 -->
						<view class="address">{{ orderType == 'takeout' ? address.complete_address : '中心城店' }}</view>
						<image src="/static/images/common/black_arrow_right.png" class="right-icon"></image>
					</view>
					<!-- 外卖&自取switch begin -->
					<view class="buttons">
						<button type="default" class="button" 
								:class="{active: orderType == 'takein'}" plain 
								hover-class="none" @tap="switchOrderType">
							自取
						</button>
						<button type="default" class="button" 
								:class="{active: orderType == 'takeout'}" plain 
								hover-class="none" @tap="switchOrderType">
							外卖
						</button>
					</view>
					<!-- 外卖&自取switch end -->
				</view>
				<view class="location">距离您622m</view>
			</view>
			</view>
			</view>
</template>

<script>
</script>

<style lang="scss">
	@import './index.scss';
</style>
