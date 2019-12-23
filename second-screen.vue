<template>
	<div id="screen2">
		<div class="phone-app-block">
			<div class="phone-app-block-description">
				<img src="/assets/app/build/zdoroviya_dnevnik_msk/phone.png" alt="">
				<div class="phone-app-block-description-text">
					<div class="phone-app-block-description-text-title">
						<p>Что такое «Дневник здоровья»?</p>
					</div>
					<div class="phone-app-block-description-text-other">
						<p>Дневник пациента — это удобный онлайн-сервис:</p>
						<ul>
							<li><p>Вносите результаты измерений вручную или с помощью <br>интегрированных приборов</p></li>
							<li><p>Ведите персональную медицинскую карту с историей <br> ваших измерений </p></li>
							<li><p>Делитесь результатами измерений со специалистами <br>для повышения эффективности лечения</p></li>
							<li><p>Получайте рекомендации, созданные специально для вас</p></li>
						</ul>
					</div>
					<div class="phone-app-block-description-btn">
						<a href="#" style="display:block;font-size:16px;color:white;text-decoration:none;font-family: 'Open Sans', sans-serif;padding:15px;">Оставить заявку</a>
					</div>
				</div>				
			</div>					
		</div>
		<img src="/assets/app/build/zdoroviya_dnevnik_msk/pusle.png" alt="" id="pulse">
	</div>
</template>
<script>
	export default{

	}
</script>
<style>
	#screen2{
		overflow: hidden;
		text-align: center;
		width:100vw;
		height: auto;
		position:relative;
	}
	.phone-app-block{
		position:relative;
	}
	.phone-app-block-description{
		display: flex;
		justify-content: center;		
	}
	.phone-app-block-description-text{
		text-align:left;
	}
	.phone-app-block-description-text-title{
		font-size: 36px;
	    font-family: 'Open Sans', sans-serif;
	    line-height: 54px;
	    color:#60759d;
	}
	.phone-app-block-description-text-other{
		font-size:16px;
		color:#60759d;
	}
	.phone-app-block-description-text ul{
		display:block;
		color:#16afe0;
		padding:15px;
	}
	.phone-app-block-description-text p{
		color:#60759d;
	}
	.phone-app-block-description-btn{
		display:inline-block;
		border-radius:100px;
		background-color:#e70067;
		padding:5px 25px;
		transition:all 0.2s;
	}
	#pulse{
		position:absolute;bottom:0;right:5%;;
	}
	@media (min-width: 250px) and (max-width: 1000px){
		.phone-app-block-description{
			display:inline-block;
		}
		.phone-app-block-description-text{
			text-align:center;
		}
		#screen2{
			height:unset;
		}
		.phone-app-block-description-text ul{
			text-align:left;
			padding:22px;
		}
		#pulse{
			bottom: 29%;
			z-index:-1;
		}
		.phone-app-block-description img{
			margin-top:5rem;
			float:right;
		}
	}
</style>