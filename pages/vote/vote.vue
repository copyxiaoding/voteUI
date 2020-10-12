<template>
		<view class="vote2">
			<!-- 顶部视图 -->
			<view class="topactive">
				<view class="stripes">
					<view class="titletop">
						<view class="titletop-left">
							<text>{{titletopname}}</text>
						</view>
						<view class="titletop-right">
								<text>开始投票</text>	
							<view class="titletoptime">
								<text>投票时间：{{votetime}}</text>					
							</view>
						</view>							 												
					</view>					 
				</view>          			
			</view>
			
			<!-- 活动视图 -->
			<view class="second">
				<view class="introduceborder">
					<view class="introduce">
						<!-- <view class="introduce-name">
							<img src="../../static/1.png" width="100%" height="100%"></image>
						</view> -->
						<view class="introduce-name">活动介绍</view>
						<view class="introduce-time">-活动时间-</view>
						<view class="introduce-time2">{{time}}</view>
						<view class="introduce-state">{{state}}</view>
						<view class="introduce-time2">-进展情况-</view>
						<view class="introduce-statistics">
							<table border="1" >
								<tr>												
									<th>候选项</th>
									<th>投票人次</th>
									<th>访问量</th>														
								</tr>
								<tr>
									<td>12</td>
									<td>433523</td>
									<td>35235213</td>
								</tr>						
							</table>
						</view>
					</view>
				</view>
			</view>
			
			
			<!-- 选择视图 -->
			<view class="box3">				
					<!-- <scroll-view class="sort1" scroll-x>
						<view
						@click="changesort(item.id)"
						:class="active===index?'active':''" 
						v-for="(item,index) in sort" 
						:key="item.id">
						{{item.name}}
						</view>		
					</scroll-view>		
					<scroll-view class="right" scroll-y>
						<view class="item" v-for="item in secondData" :key="item.id">
							<image @click="previewImg(item.img_url)" :src="item.img_url"></image>	
							<text>{{item.title}}</text>
						</view>
							<text v-if="secondData.length===0">暂无数据</text>
					</scroll-view> -->
				
				<!-- <view class="sort" v-for="(item,index) in buttonlist" :key="index">
					<view class="sortitem">{{item.name}}</view>				
				</view> -->
				<view class="sort">
					<view 
					v-for="(item,index) in buttonlist" 
					@click="changesort(index,item.id)"
					:class="active===index?'active':''" 
					:key="item.id">
					{{item.name}}</view>
					<!-- <view>1</view>
					<view>1</view> -->
				</view>
				<!-- 搜索视图 -->
				<view class="search">
					<view class="input">
						<input type="text" placeholder="请输入候选人姓名或编号" />
					</view>
					<view class="button">
						<button>搜索</button>
					</view>
				
				</view>	
				<!-- 列表视图 -->
				<view class="magelist">
					<view class="maglist-show" v-for="item in meslist" :key="item.id">			
						<view class="show-introduce" >			
							<view class="intro-img">
								{{item.intronum}}号选手
							</view>
							<img v-bind:src="item.imgUrl" width="100%" ></img>
							<view class="intro-name">
								{{item.introname}}
							</view>
							<view class="intro-address">
								{{item.introaddress}}
							</view>
							<view class="intro-detail">
								{{item.introdetail}}
							</view>
							<hr/>
						</view>
						<view class="show-statistics">
							<view class="static-num">
								投票数:{{item.staticnum}}
							</view>
							<view class="static-middle">
								<view class="static-rank">
									排名:{{item.ranknum}}
									占比:{{item.rankprop}}
								</view>		
							</view>	
							<hr/>
							<view class="toupiao">
								<button>投一票</button>
							</view>	
						</view>
					</view>
					<view class="maglist-show-r">
						
					</view>		
				</view>
			</view>
			
			
			
					
			
		</view>		
</template>

<script>
	export default {
		data() {
			return {
				active:0,
				titletopname:"评选最美员工",
				votetime:"07.15-08.30",
				time:"2020/01/12 12:00-2020/01/15 15:00",
				state:"已开始",
				id:1,
				buttonlist:[
					{
						id:1,
						name:"俱乐部"
						
					},
					{
						id:2,
						name:"球员"
						
					},
					{
						id:3,
						name:"球队"
						
					}
				],
				meslist:[
					{
						imgUrl:"../../static/A.png",
						typeid:1,
						intronum:"1",
						introname:"哆啦A梦",
						introaddress:"大阪",
						introdetail:"了解更多",
						staticnum:"4545454",
						ranknum:"1",
						rankprop:"89%",
						id:1
					},
					{
						imgUrl:"../../static/A.png",
						typeid:1,
						intronum:"1",
						introname:"哆啦A梦",
						introaddress:"大阪",
						introdetail:"了解更多",
						staticnum:"4545454",
						ranknum:"1",
						rankprop:"89%",
						id:1
					},
					{
						imgUrl:"../../static/A.png",
						typeid:1,
						intronum:"1",
						introname:"哆啦A梦",
						introaddress:"大阪",
						introdetail:"了解更多",
						staticnum:"4545454",
						ranknum:"1",
						rankprop:"89%",
						id:1
					}
				],
				meslist1:[
					{
						imgUrl:"../../static/A.png",
						typeid:1,
						intronum:"1",
						introname:"哆啦A梦",
						introaddress:"大阪",
						introdetail:"了解更多",
						staticnum:"4545454",
						ranknum:"1",
						rankprop:"89%",
						id:1
					},
					{
						imgUrl:"../../static/A.png",
						typeid:1,
						intronum:"1",
						introname:"哆啦A梦",
						introaddress:"大阪",
						introdetail:"了解更多",
						staticnum:"4545454",
						ranknum:"1",
						rankprop:"89%",
						id:1
					},
					{
						imgUrl:"../../static/A.png",
						typeid:1,
						intronum:"1",
						introname:"哆啦A梦",
						introaddress:"大阪",
						introdetail:"了解更多",
						staticnum:"4545454",
						ranknum:"1",
						rankprop:"89%",
						id:1
					}
				],
				meslist2:[
					{
						imgUrl:"../../static/B.png",
						typeid:1,
						intronum:"1",
						introname:"哆啦A梦",
						introaddress:"大阪",
						introdetail:"了解更多",
						staticnum:"4545454",
						ranknum:"1",
						rankprop:"89%",
						id:1
					},
					{
						imgUrl:"../../static/B.png",
						typeid:1,
						intronum:"1",
						introname:"哆啦A梦",
						introaddress:"大阪",
						introdetail:"了解更多",
						staticnum:"4545454",
						ranknum:"1",
						rankprop:"89%",
						id:1
					},
					{
						imgUrl:"../../static/B.png",
						typeid:1,
						intronum:"1",
						introname:"哆啦A梦",
						introaddress:"大阪",
						introdetail:"了解更多",
						staticnum:"4545454",
						ranknum:"1",
						rankprop:"89%",
						id:1
					}
				],
				meslist3:[
					{
						imgUrl:"../../static/C.png",
						typeid:1,
						intronum:"1",
						introname:"哆啦A梦",
						introaddress:"大阪",
						introdetail:"了解更多",
						staticnum:"4545454",
						ranknum:"1",
						rankprop:"89%",
						id:1
					},
					{
						imgUrl:"../../static/C.png",
						typeid:1,
						intronum:"1",
						introname:"哆啦A梦",
						introaddress:"大阪",
						introdetail:"了解更多",
						staticnum:"4545454",
						ranknum:"1",
						rankprop:"89%",
						id:1
					},
					{
						imgUrl:"../../static/C.png",
						typeid:1,
						intronum:"1",
						introname:"哆啦A梦",
						introaddress:"大阪",
						introdetail:"了解更多",
						staticnum:"4545454",
						ranknum:"1",
						rankprop:"89%",
						id:1
					}
				]
			}
		},	
		methods: {
			change:function(){
				alert("sgsahgfasgsa")
			},
			qiehuan:function(){
				alert("我是俱乐部")
			},
			changesort(index,id){
				this.active=index
				console.log(id)
				if(id==1){
					this.meslist=this.meslist1
				}else if(id==2){
					this.meslist=this.meslist2
				}else{
					this.meslist=this.meslist3
				}
			}
		}
	}
</script>

<style lang="scss">
	.vote2{
		background: #fefccc;
		width: 750rpx;
		.topactive{//顶部
			width: 100%;
			height: 300rpx;
			background: #ffed74;
				.stripes {//黑白斜条纹
					height: 200rpx;
					width: 500rpx;
					position: absolute; //固定值
					margin: 60rpx 110rpx 40rpx 140rpx;
					//斜纹（角度，斜纹颜色，背景颜色，斜纹空隙大小）
					background: repeating-linear-gradient(45deg, #000000, #ffffff 6px);
					border:solid 1px #000;
						.titletop{//开始投票
							width: 500rpx;
							height: 200rpx;
							background: #ffd022;
							margin-left: -6%;
							margin-top: -6%;
							display: flex;//横向布局
							// flex-direction: row;//横向布局 				
							border:solid 1px #000;
							color:#000000;
							.titletop-left{//顶部左边
								width:  50rpx;
								height: 200rpx;
								background: #ff8c89;
								margin-left: 2%;
								border-right:solid 2px #000;					
								text{//投票名称
									font-weight:500rpx;
									font-size:30rpx;
									text-align:center; 
									line-height:16px;
									writing-mode:tb-rl//竖向排列
								}
							}
							.titletop-right{//	顶部右边
								width:  450rpx;
								height: 200rpx;						
								padding-top: 30rpx;
								text-align: center;	
								text{//开始投票
									font-weight:bold;
									font-size:70rpx;								
								}
								.titletoptime{//投票时间	
									background: #fff;
									width:340rpx;
									margin: 0 auto;
									text{
										text-align: center;
										font-size: 30rpx;
									}
								}
							}
						}
				}
		
		}
		.second{//活动介绍
			width: 750rpx;
		
			margin:30rpx 0 30rpx 0;			
			.introduceborder{
				width: 560rpx;
				margin: 0 auto;
				background: #fee2b0;
				border-radius: 20px;
				padding-top:25rpx ;				
				.introduce{
					width:  650rpx;
					margin: 0 -45rpx 0 -45rpx;
					background: #ffa660;
					border-radius: 25px;
					text-align: center;
					padding: 30rpx 0;
					font-size: 30rpx;
					color: #fff;
					line-height:65rpx;
					.introduce-name{
						border-radius: 60%;
						background: #FFFFFF;
						color: #ff6849;
						width:300rpx;
						margin:0 auto;	
						font-size: 35rpx;
					}
					.introduce-time{
						font-size: 35rpx;
					}
					.introduce-time2{	
					}
					.introduce-state{
						background-color: #f96734;
						width:140rpx;
						border-radius: 20rpx;
						margin:0 auto;
					}
					.introduce-statistics{
						margin:0 auto;
					} 
					table{
						margin:0 auto;
						border-collapse: collapse;
						width: 80%;
					}
					td{
						font-size:35rpx;
						font-weight: 400;	 
						border:1px solid #ff6849;
						background-color: #ffffff;
						color: #ff6849;
					}
					th
					{
						font-size:35rpx;
						font-weight: 400;
						border:1px solid #ff6849;
						background-color:#ffffff;
						color:#000000;
					}
				}
			}	
	}
		.box3{
			width: 750rpx;
			margin-top: 10rpx;
			.sort{
				display: flex;
				margin: 0 50rpx 30rpx 50rpx;
				view{
					font-size: 33rpx;
					text-align: center;
					border: 1px;
					width:140rpx;
					margin-left: 10rpx;
					border:solid 1px #ff6849;
					color: #ff6849;
					border-radius: 10rpx;
			}	
				.active{
				background: #ff6849;
				color: #fff
				}
		}
			.search{
				width:140rpx;
				display: flex;
				margin: 0 50rpx 30rpx 50rpx;
				.input {					
					input{
						background: #ffffff;
						width: 530rpx;
						height: 70rpx;
						border-radius: 10rpx;
						
					}
				}
				.button{
					button{
						background: #ff6849;
						text-align: center;
						font-size: 30rpx;
						color: #fff;
						width: 120rpx;
						height: 70rpx;
						border-radius: 10rpx;
					}
				}
			}		
			.magelist{//信息列表
				width:640rpx;
				display: flex;
				flex-wrap:wrap;
				margin: 0 auto;
				.maglist-show{//白色背景
					width: 300rpx;
					background-color: #ffffff;
					margin:10rpx;
					.intro-img{
						background:#ff6849 ;
						font-size:30rpx;
						text-align: center;
						width: 150rpx;
						margin: 0 auto;
						color: #ffffff;						
					}
				}
				.intro-name{//名字
					font-weight: 300rpx;
					font-size: 40rpx;
					color: #ff6849;
					text-align: center;
				}
				.intro-address{//地点
					width: max-content;
					font-size:medium;
					color: #b0a4ae;
					margin: 0 auto;
				}
				.intro-detail{//了解详情
					width: max-content;
					font-size:small;
					text-decoration:underline;//下滑线
					color: #ff6849;
					margin: 0 auto;
				}
				.static-num{//投票数
					width: max-content;
					font-size:small;
					color: #ff6849;
					margin: 0 auto;
				}
				.static-rank{//占比
					width: max-content;
					font-size:small;
					color: #ff6849;
					margin: 0 auto;
				}
				.toupiao {//按钮
					width: 300rpx;
					button{				
					width: 200rpx;
					background: #ff6849;	
					color: #fff;
					font-size: 25rpx;
					border-radius: 70rpx;
					margin: 10rpx 50rpx;
					}
				}
			}
					
		}
}
</style>
