<template>
  <div id="app">
       <view-box>
       			   <x-header :left-options="{showBack: false}" :right-options="{showMore: true}">酷狗音乐</x-header>
       			  <!--<x-header :right-options="{showMore: true}" @on-click-more="showMenus = true">with more menu</x-header>-->
       			<tab>
       			   	  <tab-item selected>新歌</tab-item>
       			   	  <tab-item>排行</tab-item>
       			   	  <tab-item>歌单</tab-item>
       			   	  <tab-item>歌手</tab-item>
       			</tab>
       			<!--<swiper :list="list" auto style="width:100%;margin:0 auto;" dots-position="center" ></swiper>-->
       			<swiper :list="list" :index="demo06_index" @on-index-change="demo06_onIndexChange"></swiper>
       			<!--<router-view></router-view>-->
			      <!--<tabbar> 			    	
						     <tabbar-item >
						        <span slot="label"><router-link to="/">Mes</router-link></span>
						      </tabbar-item>
						      <tabbar-item show-dot>
						        <span slot="label"><router-link to="/one">Mes</router-link></span>
						      </tabbar-item>
						      <tabbar-item selected>
						        <span slot="label"><router-link to="/three">Explore</router-link></span>
						      </tabbar-item>
						      <tabbar-item badge="2">
						        <span slot="label">News</span>
						      </tabbar-item>
			      </tabbar>-->
			    
       </view-box>
       
  </div>
</template>
<script>
import {ViewBox} from 'vux'
import { XHeader } from 'vux'
import { Tab, TabItem } from 'vux'
import { Swiper } from 'vux'
import { Tabbar, TabbarItem } from 'vux'
import { Panel } from 'vux'
export default {
name: 'app',
components:{
	ViewBox,XHeader,Tab, TabItem,Swiper,Tabbar, TabbarItem,Panel
},
	data(){
		return{
			list:[{
				  url: 'javascript:',
				  img: 'https://static.vux.li/demo/1.jpg',
				  title: '送你一朵fua'
				}, {
				  url: 'javascript:',
				  img: 'https://static.vux.li/demo/2.jpg',
				  title: '送你一辆车'
				}, {
				  url: 'javascript:',
				  img: 'https://static.vux.li/demo/3.jpg',
				  title: '送你一次旅行',
				  fallbackImg: 'https://static.vux.li/demo/3.jpg'
				}],
				      demo06_index: 0,
		}
	},
  
//	methods:{
//		demo07_onIndexChange (index) {
//    this.demo07_index = index
//  }
//	}
	methods: {
    demo06_onIndexChange (index) {
      this.demo06_index = index
    }
  }
}

</script>

<style lang="less">
@import '~vux/src/styles/reset.less';
html,body{
	margin:0;
	width:100%;
	height: 100%;
	overflow-x: hidden;
}
.vux-header{
	background-color: red!important;
}
#app {
    height: 100%;
}
.vux-tab-item{
	font-size: 20px!important;
	/*!important;*/
}
.vux-tab .vux-tab-item.vux-tab-selected {
	color:blue!important;
	font-size: 20px!important;
}
</style>