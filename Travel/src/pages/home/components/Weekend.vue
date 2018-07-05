<template>
	<div>
	  <div class="title">周末去哪</div>
	  <ul>
	  	<li class="item border-bottom" v-for="item of recommendList" :key="item.id">
	  		<div class="item-img-wrapper">
	  			<img class="item-img" :src="item.imgUrl">
	  		</div>
	  		<div class="item-info">
		  		<p class="item-title">{{item.title}}</p>
		  		<p class="item-desc">{{item.desc}}</p>
	  		</div>
	  	</li>
	  </ul>
	</div>
</template>

<script>
export default {
	name: 'HomeWeekend',
	data () {
		return {
			recommendList: [{
				id: '0001',
				imgUrl: 'http://img1.qunarzz.com/sight/source/1508/f8/cadd4e229d3402.jpg_r_640x214_c38fb221.jpg',
				title: '佛山必游TOP10',
				desc: '走进佛山河网密布，生态优美的岭南水乡',
			}, {
				id: '0002',
				imgUrl: 'http://img1.qunarzz.com/sight/source/1602/88/bf120edeaea383.jpg_r_640x214_f8591f7b.jpg',
				title: '欢乐长隆',
				desc: '世界欢乐汇聚长隆',
			}, {
				id: '0003',
				imgUrl: 'http://img1.qunarzz.com/sight/source/1511/f7/90c1c5f6f3dd59.jpg_r_640x214_3cb4974e.jpg',
				title: '河源必游TOP10',
				desc: '走进客家古邑，感受万绿河源',
			}]
		}
	}
}
</script>

<style lang="stylus" scoped>
  @import '~styles/mixins.styl'
  .title
    line-height: .8rem
    background: #eee
    text-indent: .2rem
  .item-img-wrapper
    overflow: hidden
    height: 0
    padding-bottom: 37.09%
    .item-img
      width: 100%
  .item-info
    padding: .1rem
    .item-title
      line-height: .54rem
      font-size: .32rem
      ellipsis()
    .item-desc
      line-height: .4rem
      color: #ccc
      ellipsis() 
</style>