<template>
	<view>
		<view class="box">
			<!-- 顶部视图 -->
			<view class="topactive">
				<view class="stripes">
					<view class="titletop">
						<view class="titletop-left">
							<view class="titletopname">
								<text>评选最美员工</text>		
							</view>
						</view>
						<view class="titletop-right">
							<view class="titletopstart">
								<text>开始投票</text>	
							</view>	
							<view class="titletoptime">
								<text>投票时间：07.15-08.30</text>					
							</view>
						</view>							 												
					</view>					 
				</view>          			
			</view>
			
			<!-- 活动视图 -->
			<view class="introduceborder">
				<view class="introduce">
					<!-- <view class="introduce-name">
						<img src="../../static/1.png" width="100%" height="100%"></image>
					</view> -->
					<view class="introduce-name">活动介绍</view>
					<view class="introduce-time">-活动时间-</view>
					<view class="introduce-time2">2020/01/12 12:00-2020/01/15 15:00</view>
					<view class="introduce-state">已开始</view>
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
			
			<!-- 选择视图 -->
			<view class="sort">
				<view class="sort-left">
					俱乐部
				</view>
				<view class="sort-middle">
					球员
				</view>
				<view class="sort-right">
					球队
				</view>
				<!-- <input placeholder="请输入姓名或编号进行搜索"/> -->
			</view>
			
			<!-- 搜索视图 -->
			<view class="search">
				<input type="text" placeholder="请输入候选人姓名或编号" />
				<button>搜索</button>
				<!-- <view class="search-input">
					<input>
				</view>
				<view class="search-button">
					<button>搜索</button>
				</view> -->
			</view>	
					
			<!-- 列表视图 -->
			<view class="magelist">
				<view class="maglist-show-l">
					<img src="../../static/A.png" width="100%" height="150"></image>
		<!-- 			<table>
						<tr>
							<tr>哆啦A梦</tr>
							<tr>大阪</tr>
							<tr>
								<button>了解更多</button>
							</tr>
						</tr>
						<tr>
							<tr>投票数44134134</tr>
							<tr>
								<td>排名：1</td>
								<td>占比：89%</td>
							</tr>
						</tr>
						<tr>
							<button>投一票</button>
						</tr>
					</table> -->
					<view class="show-introduce">
						<view class="intro-name">
							哆啦A梦
						</view>
						<view class="intro-address">
							大阪
						</view>
						<view class="intro-detail">
							<!-- <a href="http:www.baidu.com">了解更多</a> -->
							了解更多
						</view>
						<hr/>
					</view>
					<view class="show-statistics">
						<view class="static-num">
							投票数：4545454
						</view>
						<view class="static-middle">
							<view class="static-rank">
								排名：1
								占比：89%
							</view>
							<!-- <view class="static-proportion">
								占比：89%
							</view> -->
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
				
			}
		},
		methods: {
			
		}
	}
</script>

<style>
	.box{
		background: #fefccc;
	}
	/* 顶部背景 */
	.topactive{
		width: 100%;
		height: 300rpx;
		background: #ffed74;
		
	}
	/* 黑白斜条纹 */
	.stripes {
	    height: 200rpx;
	    width: 70%;
		position: absolute;
	    /* float: center; */	 
	  margin-left: 17%;
	  margin-top: 10%;
	
		background: #ffffff;
	    /* -webkit-background-size: 50px 50px; */
	    /* -moz-background-size: 50px 50px; */
	    background-size: 100rpx 100rpx; /* 控制条纹的大小 */
	
	    /* -moz-box-shadow: 1px 1px 8px gray; */
	    /* -webkit-box-shadow: 1px 1px 8px gray; */
	   /* box-shadow: 1px 1px 8px #010101; /*控制条纹阴影*/
		background: repeating-linear-gradient(45deg, #000000, #ffffff 6px);	
		border:solid 1px #000;
	}
	/* 开始投票背景 */
	.titletop{
		width: 100%;
		height: 200rpx;
		background: #ffd022;
		margin-left: -6%;
		margin-top: -6%;
		flex-direction: row;/* 横向布局 */
		position: relative;
		border:solid 1px #000
	}
	/* 顶部左边 */
	.titletop-left{
		width:  10%;
		height: 100%;
		background: #ff8c89;
		margin-left: 2%;
		border-right:solid 2px #000
	}
	/* 投票名称 */
	.titletopname{
		font-weight:500rpx;
		font-size:smaller;
		/* writing-mode:rl-tb; */
		text-align:center; 
		line-height:16px
	}
	/* 顶部右边 */
	.titletop-right{	
		/* padding-top: 15%;
		padding-left: 2%; */
		width:  100%;
		height: 100%;
		margin-top: -45%;
		/* position: relative; */
	}
	/* 投票时间 */
	.titletoptime{
		font-weight:100rpx;
		font-size: 70%;
		width:  60%;
		height: 30%;
		margin-left: 25%; 
		background: #ffffff;
	}
	/* 开始投票 */
	.titletopstart{
		font-weight:bold;
		font-size: 200%;
		padding-top: 10%;
		padding-left: 25%;
		}
	/* 点击变换 */
	/* .box-active{
		background:#007AFF;
	} */
	
	/* 活动介绍边框 */
	.introduceborder{
		width:  80%;
		height:360rpx;
		padding-top: 20rpx;
		padding-bottom: 20rpx;
		margin-left: 10%;
		margin-top:25rpx;
		margin-bottom: 40rpx;
		/* margin-left: 5%; */
		background: #fee2b0;
		border-radius: 25px;
		position: absolute;
		
	}
	/* 活动介绍背景 */
	.introduce{
		font-size: medium;
		width:  110%;
		height: 110%;
		background: #ffa660;
		margin-left: -5%;
		/* padding-top:25px solid #fee2b0; */
		border-radius: 25px;
		color: #ffffff;/* 介绍框中颜色全为白 */
		text-align: center;
		position: relative;		
		padding-top: 20rpx;
		 
		 /* bottom: calc(var(--introduceborder-bottom) + 50px)
		 
		 /* padding-top: 200px; */
		/* margin-bottom: 40rpx; */
		 /* border-top: 8rpx solid #fee2b0; */
	}
	.introduce-name{
		background-color: #FFFFFF;
		color: #ff6849;
		width:50%;
		border-radius: 50%;/* 椭圆 */
		margin:0 auto;/* 水平居中 */
		/* margin-top: 10rpx; */
		margin-bottom: 10rpx;
	}
	.introduce-time{
		margin-bottom: 10rpx;
	}
	.introduce-time2{
		margin-bottom: 10rpx;
	}
	.introduce-state{
		background-color: #f96734;
		color: #ffffff;
		width:20%;
		border-radius: 10rpx;
		margin:0 auto;
		margin-bottom: 10rpx;
	}
	.introduce-statistics{
		margin:0 auto;
	}
/* 	.introduce-statistics{
		table{
			border-collapse: collapse;
			border:1px solid #ff6849;
			background-color: #ffffff;
			color: #ff6849;
		}
	} */
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
	/* 点击变换 */
	/* .box2-active{
		background:pink;
	}
	
	/* 类型选择 */
	.sort{
		font-size: medium;
		width: 100%;
		height: 5%;
		/* background: #ff6849; */
		margin-top:64%;
		margin-bottom: 25%;
		/* padding-top: 20rpx;
		padding-bottom: 20rpx; */
		flex-direction: row;/* 横向布局 */
		position: absolute;
		
	}
	.sort-left{
		width:80%;
		height: 100%;
		border:solid 2px #ff6849;
		color: #ff6849;
		display:inline;
		margin-left:7%;
		margin-right:3%;
		padding-left: 2%;
		padding-right: 2%;
		border-radius: 3px;
	}
	.sort-middle{
		width:80%;
		height: 100%;
		border:solid 2px #ff6849;
		color: #ff6849;
		display:inline;
		margin-right:3%;
		padding-left: 2%;
		padding-right: 2%;
		border-radius: 3px;
	}
	.sort-right{	
		width:80%;
		height: 100%;	
		border:solid 2px #ff6849;
		color: #ff6849;
		padding-left: 2%;
		padding-right: 2%;
		display:inline;
		border-radius: 3px;
	}
	.search{
		margin-top: 73%;
		margin-left: 7%;
		width:  86%;
		display: inline-block;
		height: 35px;
		overflow: auto;
		background-color: #ffffff;

	}
	.search input{	
		padding: 0px 10px;
		float: left;
		height: 33px;
		line-height: 33px;	
	}
	.search button{	
		float: right;		
		line-height: 31px;	
		background: #ff6849;	
		color: #fff;
		font-size: small;
	}
	/* 信息列表 */
	.magelist{
		margin-top: 2%;
		margin-left: 7%;
		width:  86%;
		height: auto;
		display: inline-block;/* 线性布局 */
		height: 35px;
		background-color: #fefccc;
		
	}
	.maglist-show-l{
		width:  49%;
		display: inline-block;
		overflow: auto;
		background-color: #ffffff;
		margin-right: 1%;
	}
	.intro-name{
		width: max-content;	
		font-size: 40rpx;
		color: #ff6849;
		margin: 0 auto;
	}
	.intro-address{
		width: max-content;
		font-size:medium;
		color: #b0a4ae;
		margin: 0 auto;
	}
	.intro-detail{
		width: max-content;
		font-size:small;
		text-decoration:underline;/* 下划线 */
		color: #ff6849;
		margin: 0 auto;
	}
	.static-num{
		width: max-content;
		font-size:small;
		color: #ff6849;
		margin: 0 auto;
	}	
	.static-rank{
		width: max-content;
		font-size:small;
		color: #ff6849;
		margin: 0 auto;
	}
	.toupiao button{
		width: 70%;
		line-height: 35px;	/* 和内容之间的距离 */
		background: #ff6849;	
		color: #fff;
		font-size: small;
		border-radius: 70rpx;
	}
/* 	.static-middle{
		
	} */
/* 	.static-proportion{
		display: inline-block;
	} */
/* 	.maglist-show-r{
		width:  49%;
		display: inline-block;
		
		overflow: auto;
		background-color: #ffffff;
		margin-left: 1%;
	} */

</style>
