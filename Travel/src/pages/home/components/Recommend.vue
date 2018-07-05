<template>
	<div>
	  <div class="title">热销推荐</div>
	  <ul>
	  	<li class="item border-bottom" v-for="item of recommendList" :key="item.id">
	  		<img class="item-img" :src="item.imgUrl">
	  		<div class="item-info">
		  		<p class="item-title">{{item.title}}</p>
		  		<p class="item-desc">{{item.desc}}</p>
		  		<button class="item-button">查看详情</button>
	  		</div>
	  	</li>
	  </ul>
	</div>
</template>

<script>
export default {
	name: 'HomeRecommend',
	data () {
		return {
			recommendList: [{
				id: '0001',
				imgUrl: 'http://img1.qunarzz.com/sight/p0/1708/73/73cedba65c6e4e40a3.water.jpg_200x200_0f67bb83.jpg',
				title: '李小龙乐园',
				desc: '好玩的李小龙',
			}, {
				id: '0002',
				imgUrl: 'http://img1.qunarzz.com/sight/p0/1706/ee/eeae6f60b67e85dea3.water.jpg_200x200_33846265.jpg',
				title: '顺德史努比公园',
				desc: '好玩的小孩子乐园',
			}, {
				id: '0003',
				imgUrl: 'http://img1.qunarzz.com/sight/p0/1707/3f/3f85f2697cd4b2d1a3.water.jpg_200x200_65dd55b7.jpg',
				title: '美的鹭湖探索王国',
				desc: '看动物喔',
			}]
		}
	}
}
</script>

<style lang="stylus" scoped>
  @import '~styles/mixins.styl'
  .title
    margin-top: .2rem
    line-height: .8rem
    background: #eee
    text-indent: .2rem
  .item
     overflow: hidden
     display: flex
     height: 1.9rem
     .item-img
       width: 1.7rem
       height: 1.7rem
       padding: .1rem
     .item-info
       flex: 1
       padding: .1rem
       min-width: 0
       .item-title
         line-height: .54rem
         font-size: .32rem
         ellipsis()
       .item-desc
         line-height: .4rem
         color: #ccc
         ellipsis()
       .item-button
         line-height: .44rem
         margin-top: .16rem
         background: #ff9300
         padding: 0 .2rem
         border-radius: .06rem
         color: #fff    
</style>