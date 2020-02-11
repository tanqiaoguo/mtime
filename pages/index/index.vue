<template>
	<view class="content">
		<view class="banner">
			<swiper class="card-swiper" :class="dotStyle?'square-dot':'round-dot'" :indicator-dots="true" :circular="true"
			 :autoplay="true" interval="5000" duration="500" @change="cardSwiper" indicator-color="#8799a3"
			 indicator-active-color="#0081ff">
				<swiper-item v-for="(item,index) in swiperList" :key="index" :class="cardCur==index?'cur':''">
					<view class="swiper-item">					
						<image :src="item.url" mode="aspectFill" v-if="item.type=='image'"></image>
						<video :src="item.url" autoplay loop muted :show-play-btn="false" :controls="false" objectFit="cover" v-if="item.type=='video'"></video> 
					</view>
				</swiper-item>
			</swiper>
		</view>
		<!-- 1.定义属性名为title-bar的容器 包裹正一部分的内容 -->
		<view class="header">
			<!-- 2.引入color ui的图标组件 -->
			<text class="lg text-gray cuIcon-hot icon" ></text>
			<!-- 3.使用uni-app内容组件text放置文字内容 -->
			<text class="title">热门电影</text>
		</view>
        <view class="scroll-channel">
            <scroll-view class="scroll-view" scroll-x="true" >
                <view class="scroll-item">
					<view class="pic">
						<image  src="https://img1.doubanio.com/view/photo/s_ratio_poster/public/p2557573348.jpg" ></image>
					</view>
					<view class="title">
千与千寻  / 千と千尋の神隠し  / 神隐少女(台) / 千与千寻的神隐							
					</view>
					<view class="rate">
					<uni-rate color="#c3c3c3" max="5" value="4.5" size=11>8.9</uni-rate>
					<text class="score">8.9</text>
					</view>
				</view>
				<!--2 -->
				 <view class="scroll-item">
				 	<view class="pic">
				 		<image  src="https://img1.doubanio.com/view/photo/s_ratio_poster/public/p2557573348.jpg" ></image>
				 	</view>
				 	<view class="title">
				 千与千寻  / 千と千尋の神隠し  / 神隐少女(台) / 千与千寻的神隐							
				 	</view>
				 	<view class="rate">
				 	<uni-rate color="#c3c3c3" max="5" value="4.5" size=11>8.9</uni-rate>
				 	<text class="score">8.9</text>
				 	</view>
				 </view>
				<!--3 -->
				 <view class="scroll-item">
				 	<view class="pic">
				 		<image  src="https://img1.doubanio.com/view/photo/s_ratio_poster/public/p2557573348.jpg" ></image>
				 	</view>
				 	<view class="title">
				 千与千寻  / 千と千尋の神隠し  / 神隐少女(台) / 千与千寻的神隐							
				 	</view>
				 	<view class="rate">
				 	<uni-rate color="#c3c3c3" max="5" value="4.5" size=11>8.9</uni-rate>
				 	<text class="score">8.9</text>
				 	</view>
				 </view>
				<!--4 -->
				 <view class="scroll-item">
				 	<view class="pic">
				 		<image  src="https://img1.doubanio.com/view/photo/s_ratio_poster/public/p2557573348.jpg" ></image>
				 	</view>
				 	<view class="title">
				 千与千寻  / 千と千尋の神隠し  / 神隐少女(台) / 千与千寻的神隐							
				 	</view>
				 	<view class="rate">
				 	<uni-rate color="#c3c3c3" max="5" value="4.5" size=11>8.9</uni-rate>
				 	<text class="score">8.9</text>
				 	</view>
				 </view>
				<!--5 -->
				 <view class="scroll-item">
				 	<view class="pic">
				 		<image  src="https://img1.doubanio.com/view/photo/s_ratio_poster/public/p2557573348.jpg" ></image>
				 	</view>
				 	<view class="title">
				 千与千寻  / 千と千尋の神隠し  / 神隐少女(台) / 千与千寻的神隐							
				 	</view>
				 	<view class="rate">
				 	<uni-rate color="#c3c3c3" max="5" value="4.5" size=11>8.9</uni-rate>
				 	<text class="score">8.9</text>
				 	</view>
				 </view>
				<!--6 -->
				 <view class="scroll-item">
				 	<view class="pic">
				 		<image  src="https://img1.doubanio.com/view/photo/s_ratio_poster/public/p2557573348.jpg" ></image>
				 	</view>
				 	<view class="title">
				 千与千寻  / 千と千尋の神隠し  / 神隐少女(台) / 千与千寻的神隐							
				 	</view>
				 	<view class="rate">
				 	<uni-rate color="#c3c3c3" max="5" value="4.5" size=11>8.9</uni-rate>
				 	<text class="score">8.9</text>
				 	</view>
				 </view>																
            </scroll-view>		
        </view>
	<!-- 热门预告 -->
	<view class="header">
		<text class="lg text-gray cuIcon-hot icon" ></text>
		<text class="title">电影预告</text>
	</view>
	<!-- vedio-channer -->
		<view class="video-channel">
			<view class="video-item">
				<video src="" controls></video>
			</view>
			<view class="video-item">
				<video src="" controls></video>
			</view>
		</view>
		<!-- 猜你喜欢 -->
		<view class="header">
			<!-- 2.引入color ui的图标组件 -->
			<text class="lg text-gray cuIcon-hot icon" ></text>
			<!-- 3.使用uni-app内容组件text放置文字内容 -->
			<text class="title">猜你喜欢</text>
		</view>
		<view class="like-channel">
<!-- start -->
			<view class="like-item">
				<view class="img">
					<image src="https://img3.doubanio.com/view/photo/s_ratio_poster/public/p2581835383.jpg" mode=""></image>
				</view>
				<view class="detail">
					<view class="title">	
						囧妈 / 俄囧 / Lost in Russia						
					</view>
					<view class="rate">
						<uni-rate color="#c3c3c3" max="5" value="4" size=11>8.9</uni-rate>
					</view>
					<view class="msg">
						类型: 喜剧
					</view>
					<view class="time">
						2020-01-25(中国大陆网络) 
					</view>
				</view>
				<view class="star">
					<view class="icon">
						<text class="lg text-gray cuIcon-appreciate icon" ></text>
					</view>
					<view class="tile">
						赞一下				
					</view>
				</view>
			
			</view>
<!-- 2 --> 
			<view class="like-item">
				<view class="img">
					<image src="https://img3.doubanio.com/view/photo/s_ratio_poster/public/p2581835383.jpg" mode=""></image>
				</view>
				<view class="detail">
					<view class="title">	
						囧妈 / 俄囧 / Lost in Russia						
					</view>
					<view class="rate">
						<uni-rate color="#c3c3c3" max="5" value="4" size=11>8.9</uni-rate>
					</view>
					<view class="msg">
						类型: 喜剧
					</view>
					<view class="time">
						2020-01-25(中国大陆网络) 
					</view>
				</view>
				<view class="star">
					<view class="icon">
						<text class="lg text-gray cuIcon-appreciate icon" ></text>
					</view>
					<view class="tile">
						赞一下				
					</view>
				</view>
			
			</view>
<!-- 3 -->  
			<view class="like-item">
				<view class="img">
					<image src="https://img3.doubanio.com/view/photo/s_ratio_poster/public/p2581835383.jpg" mode=""></image>
				</view>
				<view class="detail">
					<view class="title">	
						囧妈 / 俄囧 / Lost in Russia						
					</view>
					<view class="rate">
						<uni-rate color="#c3c3c3" max="5" value="4" size=11>8.9</uni-rate>
					</view>
					<view class="msg">
						类型: 喜剧
					</view>
					<view class="time">
						2020-01-25(中国大陆网络) 
					</view>
				</view>
				<view class="star">
					<view class="icon">
						<text class="lg text-gray cuIcon-appreciate icon" ></text>
					</view>
					<view class="tile">
						赞一下				
					</view>
				</view>
			
			</view>
			

<!-- end	 -->
		</view>
		
	</view>
	
</template>

<script>
	import uniRate from '../../node_modules/@dcloudio/uni-ui/lib/uni-rate/uni-rate.vue';
	
	export default {
		data(){
			return{
				cardCur: 0,
				swiperList: [{
					id: 0,
					type: 'image',
					url: 'https://ossweb-img.qq.com/images/lol/web201310/skin/big84000.jpg'
				}, {
					id: 1,
					type: 'image',
					url: 'https://ossweb-img.qq.com/images/lol/web201310/skin/big37006.jpg',
				}, {
					id: 2,
					type: 'image',
					url: 'https://ossweb-img.qq.com/images/lol/web201310/skin/big39000.jpg'
				}, {
					id: 3,
					type: 'image',
					url: 'https://ossweb-img.qq.com/images/lol/web201310/skin/big10001.jpg'
				}, {
					id: 4,
					type: 'image',
					url: 'https://ossweb-img.qq.com/images/lol/web201310/skin/big25011.jpg'
				}, {
					id: 5,
					type: 'image',
					url: 'https://ossweb-img.qq.com/images/lol/web201310/skin/big21016.jpg'
				}, {
					id: 6,
					type: 'image',
					url: 'https://ossweb-img.qq.com/images/lol/web201310/skin/big99008.jpg'
				}],
				dotStyle: false,
				towerStart: 0,
				direction: ''
			}
		},
	   methods:{
		   DotStyle(e) {
		   	this.dotStyle = e.detail.value
		   },
		   // cardSwiper
		   cardSwiper(e) {
		   	this.cardCur = e.detail.current
		   }
       		   
	   },
	   components: {uniRate}

	
	}
</script>

<style lang="scss" scoped>
	
	/* 取消轮播图内边距 */
	.card-swiper uni-swiper-item{
		padding: 0;
	}

	// 头部区域
	.header{
		/* 设置头部盒子的高度以及行高,当行高与高度一样的时候,内容会自定垂直居中 */
		height: 100rpx;
		line-height: 100rpx;
		/* 设置图标的颜色 */		
		.icon{
			color:#f37b1d;
			/* 设置图标距离左右两边一定的距离 */
			margin:0  22rpx;	
		}
		.title{
			/* 	设置头部标题文字大小,文字加粗 */
			font-size: 36rpx;
			font-weight: bold;
		}
	}
	
	// 滚动区域
	.scroll-view{
		white-space: nowrap;
		/* height: 354rpx; */
		.scroll-item{
			display: inline-block;
			width: 200rpx;
			margin-right: 20rpx;
			/* height: 354rpx; */
			/* margin: 0 20rpx; */
		/* 	background-color: pink; */
			.title{
				font-size: 24rpx;
				font-weight:bold;
			     overflow: hidden;
				 margin: 10px 0;
				 text-overflow: ellipsis;
				 white-space: nowrap;
				 
			}
			.rate{
				margin-bottom: 12rpx;
				display: flex;
				align-items: center;
			}
			.score{
				margin-left: 10rpx;
				font-size: 22rpx;
				color: #808080;
				padding-bottom: 5rpx;
				
			}
			.pic{
				height: 269rpx;
				width: 100%;
				image{
					width: 100%;
					height: 100%;		
					
				}
				
			}
		}
		
	}
		
	
	/* 视频区域 */
	
		.video-channel{
			display: flex;
			justify-content: space-between;
			padding: 0 20rpx;
			height: 220rpx;
			.video-item{
			/*   flex: 1; */
			/* 	background-color: red; */
				width: 350rpx;
				height: 220rpx;
				video{
					width: 100%;
					height: 100%;
				}
			}
		}
		
		// 猜你喜欢区域
	   .like-channel{
		   height: 238rpx;
		   padding-left: 20rpx;
		   .like-item{
			   display: flex;
			   height: 238rpx;
			   margin-bottom: 30rpx;
					.img{
						width: 180rpx;
						height:238rpx;
						border-radius: 10rpx;
						overflow: hidden;
						margin-right: 28rpx;
						image{
							width:100%;
							height: 100%;
						}
					}
					.detail{
						flex: 1;
						border-right: 1rpx dashed #dedede;
						padding-right: 30rpx;
					    .title{
						    padding-top: 10rpx;
						    padding-bottom: 15rpx;
						    font-size:36rpx;
						    font-weight: bold;
						
						
					    }
					    .rate{
						    margin-bottom: 10rpx;
					    }
					    .time{
						    font-size:22rpx;
						    color: #bababa;
						    margin-bottom: 14rpx;
					    }
					    .msg{
						    color: #bababa;
						    font-size: 22rpx;
					    }
					}
					.star{
						display: flex;
						width: 158rpx;
						flex-direction: column;
						justify-content: center;
						align-items: center;
					}
		   }
	   }
</style>
