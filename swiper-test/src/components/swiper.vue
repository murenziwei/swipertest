<template>
	<div class="swiper-plugs">
		<swiper :options="swiperOption" refs="lwSwiper">
			<swiper-slide>
				<img src="../assets/logo.png" alt="" />
				
			</swiper-slide>
			
			<swiper-slide>
				<img src="../assets/logo.png" alt="" />
				
			</swiper-slide>
			
			<swiper-slide>
				<img src="../assets/logo.png" alt="" />
				
			</swiper-slide>
			<!--分页器-->
			<div class="swiper-pagination" slot="pagination"></div>
			<!--前进后退按钮-->
			<div class="swiper-button-prev" slot="button-prev"></div>
			<div class="swiper-button-next" slot="button-next"></div>
			<!--滚动条-->
			<div class="swiper-scrollbar" slot="scrollbar"></div>
			
		</swiper>
	</div>
</template>

<script>
	
	export default{
		data(){
			return {
				swiperOption: {
			         autoplay : {
				      disableOnInteraction: false, //用户操作后是否禁止自动循环
				      delay: 1000 //自动循环时间
				     }, //可选选项，自动滑动
				     speed: 1000, //切换速度，即slider自动滑动开始到结束的时间（单位ms）
				     loop:false, //循环切换
				     grabCursor: false, //设置为true时，鼠标覆盖Swiper时指针会变成手掌形状，拖动时指针会变成抓手形状
				     // setWrapperSize: true, //Swiper使用flexbox布局(display: flex)，开启这个设定会在Wrapper上添加等于slides相加的宽或高，在对flexbox布局的支持不是很好的浏览器中可能需要用到。
				     autoHeight: true,   //自动高度。设置为true时，wrapper和container会随着当前slide的高度而发生变化。   
				     scrollbar: '.swiper-scrollbar',//显示滚动条
				     mousewheelControl: true, //设置为true时，能使用鼠标滚轮控制slide滑动
				     observeParents: false, //当改变swiper的样式（例如隐藏/显示）或者修改swiper的子元素时，自动初始化swiper
				 
				     pagination: {
				      el: '.swiper-pagination',
				      // type : 'progressbar', //分页器形状
				      clickable :true, //点击分页器的指示点分页器会控制Swiper切换
				     },
				     navigation: {
				      nextEl: '.swiper-button-next',
				      prevEl: '.swiper-button-prev',
				     },       
				   }
			}
		},
		computed:{
			swiper(){
				return this.$refs.lwSwiper.swiper;
			}
		}
	}
</script>

<style>
</style>