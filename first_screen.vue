<template>
	<div id="screen1">
		<header>			
			<nav>
				<div class="first-screen-img">
					<img src="/assets/app/build/zdoroviya_dnevnik_msk/logo.png" alt="">
				</div>			
				<div class="element">
					<p @mouseover="NoActive[0].value = true" @mouseleave="NoActive[0].value = false">О сервисе</p>
					<li v-if="NoActive[0].value == true" :class='{"elementForLi":NoActive[0].value == true}'></li>
				</div>
				<div class="element">
					<p @mouseover="NoActive[1].value = true" @mouseleave="NoActive[1].value = false">Функции</p>
					<li v-if="NoActive[1].value == true" :class='{"elementForLi":NoActive[1].value == true}'></li>
				</div>
				<div class="element">
					<p @mouseover="NoActive[2].value = true" @mouseleave="NoActive[2].value = false">Возможности</p>
					<li v-if="NoActive[2].value == true" :class='{"elementForLi":NoActive[2].value == true}'></li>
				</div>
				<div class="element">
					<p @mouseover="NoActive[3].value = true" @mouseleave="NoActive[3].value = false">Партнеры</p>
					<li v-if="NoActive[3].value == true" :class='{"elementForLi":NoActive[3].value == true}'></li>
				</div>
				<p class="header_btn">Оставить заявку</p>
			</nav>
		</header>		
			<div class="container-main animated fadeIn" v-if='slide==1' @mouseover='clearSlide' @mouseleave='sliderMove' key="slide1">
				<div class="container-main-title">
					<p>Расширяем возможности предоставления<br>качественных медицинских услуг</p>
				</div>
				<div class="container-main-description">
					<p>«Дневник здоровья» – новый сервис для самоконтроля <br>показателей состояния здоровья, разработанный для<br> участников программы «Мое здоровье».</p>
				</div>
				<div class="container-main-btn">
					<a href="#" style="display:block;font-size:16px;color:white;text-decoration:none;">Узнать больше</a>
				</div>			
			</div>
			<div class="container-main animated fadeIn" v-if='slide==2' @mouseover='clearSlide' @mouseleave='sliderMove' key="slide2">
				<div class="container-main-title">
					<p>Следить за здоровьем станет проще</p>
				</div>
				<div class="container-main-description">
					<p>Скоро вы сможете находиться на связи со своим лечащим врачом <br> независимо от своего местоположения, вести дневник мониторинга <br>самочувствия, получать рекомендации по плану лечения и многое другое.</p>
				</div>
				<div class="container-main-btn">
					<a href="#" style="display:block;font-size:16px;color:white;text-decoration:none;">Узнать больше</a>
				</div>			
			</div>
		
		<div class="container-main-slider" style="margin-top:2%;">
			<div class="container-main-slider-border">
				<span @click='removeBg' :class='{"op1":slide==1}'>—</span>
				<span @click='bg' :class='{"op1":slide==2}'>—</span>
			</div>				
		</div>
	</div>
</template>
<script>
import JQuery from 'jquery'
 	let $ = JQuery
	export default{
		data(){
			return{
				NoActive:[{value:false},{value:false},{value:false},{value:false}],
				url:'/img/slide2.png',
				slide:1,
			}
		},
		mounted(){
			this.sliderMove()
		},
		methods:{
			bg(){
				this.slide = 2
				$('#screen1').addClass('screen2')
			},
			removeBg(){

				this.slide = 1

				$('#screen1').removeClass('screen2')
				
			},
			clearSlide(){
				clearInterval(this.slider)
			},
			sliderMove(){
				this.slider = setInterval(()=>{
					$('#screen1').addClass('screen2')
					this.slide++
					if (this.slide >2) {
						this.slide = 1
						$('#screen1').removeClass('screen2')
					}
				},5000)
				
			}
		}
	}
</script>
<style>

@import url('https://fonts.googleapis.com/css?family=Open+Sans&display=swap&subset=cyrillic,cyrillic-ext');
p,li{
	font-family: 'Open Sans', sans-serif;
}

	#screen1{
		transition:all 0.5s;	
		background-image:url(/assets/app/build/zdoroviya_dnevnik_msk/screen1.png);
		background-repeat:no-repeat;
		width:100vw;
		height:90vh;
		    background-size: cover;
    background-position: center;
	}
	.screen2{
		transition:all 0.5s;
		background-image:url(/assets/app/build/zdoroviya_dnevnik_msk/slide2.png)!important;
		background-repeat:no-repeat;
		width:100vw;
		height:100vh;
		background-size:contain;
	}
	header{

		padding:25px 85px;
	}
	nav{
		display:flex;
		justify-content: space-evenly;
		    align-items: center;
		color: #fdfffc;
		font-family: 'Open Sans', sans-serif;
	}
	#screen1 nav p{
		cursor:pointer;
	}
	#screen1 p:hover{

	}
	.header_btn{
		border: 1px solid #fdfffc;
	    border-radius: 100px;
	    padding: 15px 25px;
	    transition:0.3s;
	}
	.header_btn:hover{
		background-color:#5489c3;
	}
	.element{
		    position: relative;
	}
	.elementForLi{			
	    position: absolute;
	    left: 60%;
	    transform: translate(-50%,-50%);
	}
	.container-main{
	    text-align:center;
	    font-size: 36px;
	    color:white;
	    font-family: 'Open Sans', sans-serif;
	    line-height: 54px;
	}
	.container-main-description{
		font-size:20px;
		line-height:36px;
	}
	.container-main-btn{
		display:inline-block;
		border-radius:100px;
		background-color:#e70067;
		padding:0 50px;
		transition:all 0.2s;
	}
	.container-main-btn:hover{
		transform:scale(1.1);
		background-color:#c9005a;
	}
	.container-main-slider-border{
		border-radius: 100px;
	    display: inline-table;
	    border: 1px solid rgba(250,250,250,0.4);
	    line-height: 8px;
	    padding: 4px 9px;
	    font-size: 20px;
	    margin: auto 0;
	    position: absolute;
	    left: 50%;
	    top:70%;
	    color: white;
	    transform: translate(-50%,-50%);
	}
	.container-main-slider-border span{
		cursor:pointer;
		opacity:0.5;
		margin:0 5px;
	}
	.op1{
		opacity:1!important;
	}
	@media (min-width: 250px) and (max-width: 1000px){
		header{
			padding:15px;
		}
	nav{
			display:block;
			text-align:center;
		}
	#screen1{
			background-size:cover;
			height:unset;
		}
	.elementForLi{			
		    top:0;
		    left:0;
		    transform: unset;
		}
	.container-main-slider-border{
			left: -3%;
    		top: 5%;
    		transform: rotate(90deg);
		}
	}
</style>