<!--本页面由uniapp切片工具生成，uni-app切片-可视化设计工具(一套代码编译到7个平台iOS、Android、H5、小程序)，软件下载地址：http://www.ymznkf.com/new_view_669.htm -->
<template>
	<view class="content">
			<view class="msg_16">
				<!-- <view class="msg_1">
					<image v-on:click="msg_17_17_click()"  src="/static/msg/images/msg_17_17.jpg" mode="scaleToFill" border="0"    class="msg_17"></image>
					<text decode="true" class="title">消息中心</text>
				</view>
				<view class="msg_2">
					<view class="msg_12">
						<image v-on:click="icon_4_click()"  src="/static/msg/images/msg_icon_4.jpg" mode="scaleToFill" border="0"    class="icon"></image>
						<text decode="true" class="word">评论</text>
					</view>
					<view class="msg_13">
						<image v-on:click="icon_5_click()"  src="/static/msg/images/msg_icon_5.jpg" mode="scaleToFill" border="0"    class="icon"></image>
						<text decode="true" class="word">回复</text>
					</view>
					<view class="msg_14">
						<image v-on:click="icon_6_click()"  src="/static/msg/images/msg_icon_6.jpg" mode="scaleToFill" border="0"    class="icon"></image>
						<text decode="true" class="word">其它</text>
					</view>
				</view> -->
				<view class="Messages">
					<!-- <view ><u-tag v-on:click="icon_66_click()" style='display: inline-block; float: right; width: 80px;margin-right: 10px;margin-top: 10px;margin-bottom: -5px;' text="一键阅读" type="warning" plain></u-tag></view> -->
				<view v-for="(item_Messages, index) in list_Messages" :key="index" >
		
					<view class="row" v-on:click="icon_40_click(item_Messages)" >
						<image   :src="item_Messages.icon" mode="scaleToFill" border="0" class="icon"></image>
						<view class="msg_41">
							<view style="margin-top: 10px;" class="msg_42">
								<text decode="true" class="subject">{{item_Messages.subject}}</text>
								<!-- <text decode="true" class="time">{{item_Messages.time}}</text> -->
							</view>
							<view class="msg_43"  >
								<text decode="true" class="smallTitle">{{item_Messages.smallTitle}}</text>
								<text decode="true" style="margin-top: -18px;" class="vote" >{{item_Messages.vote}}</text>
							</view>
						</view>
					</view>
				</view>
				</view>
			</view>
		

		<view class="loading">{{loadingText}}</view>
		<view class="ymBbottom"></view>
	</view>
</template>

<script>
import msg from "./msg.js";
export default msg;
</script>

<style lang="scss" scoped>
   @import './msg.scss'
   
</style>