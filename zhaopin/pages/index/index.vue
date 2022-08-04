<template>
	<view class="content">
		<scroll-view scroll-y="true">
			<view class="top">
				<span>杭州方大丝绸有限公司</span>
				<span>应聘登记表</span>
			</view>
			<view class="center">
				<view class="input1">
					<span>*</span>
					<label>应聘岗位</label>
					<input type="text" placeholder="请输入">
				</view>
				<view class="input2">
					<span>*</span>
					<label>填表日期</label>
					<view>
						<uni-calendar ref="calendar" :insert="false" @confirm="confirm" />
						<button @click="open" ref="button">{{info}}
							<span class="iconfont icon-xiangxiajiantou"></span>
						</button>
					</view>
				</view>
				<view class="input1">
					<span>*</span>
					<label>姓名</label>
					<input type="text" placeholder="请输入">
				</view>
				<view class="input3">
					<span>*</span>
					<label>性别</label>
					<view>
						<button v-if="isShow" @click="choose" ref="button">请选择
							<span class="iconfont icon-xiangxiajiantou"></span>
						</button>
						<select v-else>
							<option value="">男</option>
							<option value="">女</option>
						</select>
					</view>
				</view>
				<view class="input2">
					<span>*</span>
					<label>出生日期</label>
					<view>
						<uni-calendar ref="calendar1" :insert="false" @confirm="confirm1" />
						<button @click="open1" ref="button">{{info1}}
							<span class="iconfont icon-xiangxiajiantou"></span>
						</button>
					</view>
				</view>
				<view class="input1">
					<span>*</span>
					<label>民族</label>
					<input type="text" placeholder="请输入">
				</view>
				<view class="input1">
					<span>*</span>
					<label>政治面貌</label>
					<input type="text" placeholder="请输入">
				</view>
				<view class="input3">
					<span>*</span>
					<label>婚否</label>
					<view>
						<button v-if="isShow1" @click="choose1">请选择
							<span class="iconfont icon-xiangxiajiantou"></span>
						</button>
						<select v-else>
							<option value="">已婚</option>
							<option value="">未婚</option>
						</select>
					</view>
				</view>
				<view class="input1">
					<span>*</span>
					<label>健康状况</label>
					<input type="text" placeholder="请输入">
				</view>
				<view class="input1">
					<span>*</span>
					<label>籍贯(省、市)</label>
					<input type="text" placeholder="请输入">
				</view>
				<view class="input1">
					<span>*</span>
					<label>联系方式</label>
					<input type="text" placeholder="请输入">
				</view>
				<view class="input1">
					<span>*</span>
					<label>电子邮箱</label>
					<input type="text" placeholder="请输入">
				</view>
				<view class="input1">
					<span>*</span>
					<label>学历</label>
					<input type="text" placeholder="请输入">
				</view>
				<view class="input1">
					<span>*</span>
					<label>现住地</label>
					<input type="text" placeholder="请输入">
				</view>
				<view class="input1">
					<span>*</span>
					<label>目前是否在职</label>
					<input type="text" placeholder="请输入">
				</view>
				<view class="input2">
					<span>*</span>
					<label>出生日期</label>
					<view>
						<uni-calendar ref="calendar2" :insert="false" @confirm="confirm2" />
						<button @click="open2" ref="button">{{info2}}
							<span class="iconfont icon-xiangxiajiantou"></span>
						</button>
					</view>
				</view>
				<view class="input1">
					<span>*</span>
					<label>期望薪资</label>
					<input type="text" placeholder="请输入">
				</view>
				<view class="input1">
					<span>*</span>
					<label>外语水平</label>
					<input type="text" placeholder="请输入">
				</view>
				<view class="input1">
					<span>*</span>
					<label>计算机水平</label>
					<input type="text" placeholder="请输入">
				</view>
				<view class="table">
					<span>*</span>
					<label>教育经历(请至少完整填写一行)</label>
					<table border="1" cellpadding="2" style="border-collapse:collapse">
						<tr>
							<th>时间</th>
							<th>毕业院校</th>
							<th>专业</th>
							<th>详细情况</th>
						</tr>
						<tr>
							<td></td>
							<td></td>
							<td></td>
							<td></td>
						</tr>
						<tr>
							<td></td>
							<td></td>
							<td></td>
							<td></td>
						</tr>
						<tr>
							<td></td>
							<td></td>
							<td></td>
							<td></td>
						</tr>
					</table>
				</view>

				<view class="table">
					<span>*</span>
					<label>工作经历(请至少完整填写一行,没有则写无)</label>
					<table border="1" cellpadding="2" style="border-collapse:collapse">
						<tr>
							<th>时间</th>
							<th>公司名称</th>
							<th>职务</th>
							<th>职责</th>
						</tr>
						<tr>
							<td></td>
							<td></td>
							<td></td>
							<td></td>
						</tr>
						<tr>
							<td></td>
							<td></td>
							<td></td>
							<td></td>
						</tr>
						<tr>
							<td></td>
							<td></td>
							<td></td>
							<td></td>
						</tr>
					</table>

				</view>
				<view class="input1">

					<label>个人荣誉</label>
					<input type="text" placeholder="请输入">
				</view>
				<view class="input1">

					<label>兴趣特长</label>
					<input type="text" placeholder="请输入">
				</view>
				<view class="input1">
					<span>*</span>
					<label>自我评价</label>
					<textarea cols="30" rows="10" style="border-bottom: 1px solid #eee;"></textarea>
				</view>
				<button style="width: 100%;height: 60rpx;line-height: 60rpx;background-color:#6f97bb ;">提交</button>
			</view>
		</scroll-view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				info: '请选择',
				isShow: 1,
				info1: '请选择',
				isShow1: 1,
				info2: '请选择'

			}
		},
		onLoad() {

		},
		methods: {
			open() {
				this.$refs.calendar.open();

			},
			open1() {
				this.$refs.calendar1.open();
			},
			open2() {
				this.$refs.calendar2.open();
			},
			confirm(e) {
				this.info = '请选择'
				this.info = e.fulldate
			},
			confirm1(e) {
				this.info1 = '请选择'
				this.info1 = e.fulldate
			},
			confirm2(e) {
				this.info2 = '请选择'
				this.info2 = e.fulldate
			},
			choose() {
				this.isShow = 0
			},
			choose1() {
				this.isShow1 = 0
			}
		}
	}
</script>

<style lang="scss">
	page {
		height: 100%;

		.content {
			height: 100%;

			scroll-view {
				height: 100%;
				padding-bottom: 60rpx;
			}
		}
	}

	.top {
		height: 105rpx;
		text-align: center;
		background-color: #6f97bb;
		color: white;
		padding: 10rpx 0 5rpx;

		span {
			display: block;
		}

		:nth-child(2) {
			margin-top: 10rpx;
			font-size: 28rpx;
		}
	}

	.center {
		border: 2rpx solid #eee;
		border-radius: 30rpx;

		padding: 20rpx;


		span {
			color: red;
		}

		.input1 {
			input {
				border-bottom: 1px solid #eee;
				margin-top: 10rpx;
			}

			margin: 20rpx 0;
		}

		.input2 {
			button {
				width: 100%;
				height: 60rpx;
				line-height: 60rpx;

				span {
					color: black;
				}
			}

			margin: 20rpx 0;
		}

		.input3 {
			button {
				width: 100%;
				height: 60rpx;
				line-height: 60rpx;

				span {
					color: black;
				}
			}

			select {
				width: 100%;
				height: 60rpx;
				line-height: 60rpx;
				text-align: center;
				font-size: 36rpx;
			}

		}

		.table {
			margin: 20rpx 0;
			padding-bottom: 20rpx;
			border-bottom: 1px solid #eee;

			table {
				width: 100%;

				tr {
					td {
						height: 40rpx;
					}
				}



			}
		}

	}
</style>
