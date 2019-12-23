<template>
	<div id='screen6'>
		<div id="errors">			
			<div class="success">
				<p>Успешно отправлено</p>
			</div>
			
		<div class="error">
			<p>В форме содержатся ошибки</p>	
		</div>
		</div>
		<div class="screen6-form">
			<div class="screen6-form-title">
				<h2>Получите бесплатный доступ к «Дневнику здоровья»</h2>
				<p>Оставьте свою электронную почту <br>и вы узнаете о запуске данного сервиса первым!
				</p>
			</div>
			<form>
				<input type="text" placeholder="Ваш E-mail" style='margin-right:20px;'>
				<div class="container-main-btn">
					<a href="#" @click.prevent='formSub' style="display:block;font-size:16px;color:white;text-decoration:none;padding:15px 0;">Отправить</a>
				</div>
			</form>		
		</div>
	</div>
</template>
<script>
import JQuery from 'jquery'
 	let $ = JQuery
	export default{
		data(){

		},
		methods:{
			formSub(){
				if ($('input').val() == '') {
					$('.error').css({display:'block'})
				}
				else{
					$('.error').css({display:'none'})
					$('.success').css('display','block')
					setTimeout(function(){
						$('.success').fadeOut(1000)
					},3000)
				}
			}
		}
	}
</script>
<style>
	#screen6{
		width:100vw;
		height:auto;
		position:relative;
		background-color:#e3e8f4;
		padding-bottom:85px;
	}
	.screen6-form{
		text-align:center;
	}
	.screen6-form-title {
		text-align:center;
		color:#60759d;
	}
	.screen6-form-title h2{
		padding-top:85px;
	}
	.screen6-form-title p{
		font-size: 20px;
		line-height: 36px;
	}
	#screen6 input{
		display: inline-block;
    	width: 300px;
   		height: 40px;
    	padding: .375rem .75rem;
    	font-size: 1rem;
    	font-weight: 400;
    	line-height: 1.5;
   		background-color: transparent;
    	background-clip: padding-box;
    	border: 1px solid #4f699b;
    	border-radius: 30px;
	}
	::-webkit-input-placeholder {color:gray;}
::-moz-placeholder          {color:gray;}
:-moz-placeholder           {color:gray;}
:-ms-input-placeholder      {color:gray;}
	.success{
		display:none;
		position:absolute;
		margin:auto 0;
		top:10%;
		left:50%;
		transform: translate(-50%,-50%);
		border:1px solid #60759d;
		padding:10px;
	}
	.error{
		display:none;
		position:absolute;
		margin:auto 0;
		top:10%;
		left:50%;
		transform: translate(-50%,-50%);
		border:1px solid red;
		padding:10px;
	}
	
	@media (min-width: 250px) and (max-width: 800px){
		#errors{
			text-align: center;
		}
	}
</style>