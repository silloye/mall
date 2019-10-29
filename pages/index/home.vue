<template>
	<view>
		<!-- <view>
			<image src="../../static/1.jpg"></image>
		</view>
		<view>
			<ul>
				<li>
					<div class="left">
						火锅，低价 48.9
						肥牛一碟，鸡肉一碟，蔬菜一盘
					</div>
					<div class="right">
						<image src="../../static/1.jpg"></image>
					</div>
				</li>
				<li>
					<image src="../../static/1.jpg"></image>
					第二款美食
				</li>
				<li>
					<!-- <image src="../../static/1.jpg"></image>
					第三款美食
				</li> 
			</ul>
		</view> -->
		<view class="uni-padding-wrap uni-common-mt">
		            <view class="uni-title uni-common-mt">
		                flex-direction: row
		                <text>\n横向布局</text>
		            </view>
		            <view class="uni-flex uni-column">
		                <view class="flex-item flex-item-V">
							<view class="uni-flex uni-row">
							    <view class="flex-item">
									<text>
										火锅，低价 48.9
										肥牛一碟，鸡肉一碟，蔬菜一盘
									</text>
								</view>
							    <view class="flex-item uni-bg-green"><image src="../../static/1.jpg"></image></view>
							</view>
						</view>
		                <view class="flex-item flex-item-V uni-bg-green">B</view>
		                <view class="flex-item flex-item-V uni-bg-blue">C</view>
		            </view>
		        </view>
	</view>
</template>

<script>
</script>

<style lang="scss">
	image {
		height: 100px;
		width: 100px;
	}
</style>
