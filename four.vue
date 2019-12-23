<template>
	<div id="screen4">
		<div class="screen4-block">
			<div class="screen4-block-title">
				<h2>Ведите персональный дневник мониторинга здоровья</h2>
			</div>
			<div class="screen4-block-list">
				<div class="screen4-block-list-left">
					<div>
						<img src="/assets/app/build/zdoroviya_dnevnik_msk/1.png" alt="" style='width:80px;float:left;'>
						<h4>Хранение данных</h4>						
						<p>Контролируйте и следите за динамикой изменения показателей вашего <br>здоровья. Вносите результаты измерений медицинских показателей вручную или с помощью интегрированных приборов, храните историю измерений и отслеживайте динамику состояния здоровья</p>
						<br>
						<img src="/assets/app/build/zdoroviya_dnevnik_msk/2.png" alt="" style='width:80px;float:left;'>
						<h4>Сообшение информации врачу</h4>						
						<p>Позвольте специалисту дистанционно следить за вашим здоровьем. <br>
Будьте на связи со специалистом - отправляйте информацию о своем <br>самочувствии, обменивайтесь сообщениями и получайте <br>рекомендации по вашему здоровью и лечению.</p>
						<br>
						<img src="/assets/app/build/zdoroviya_dnevnik_msk/3.png" alt="" style='width:80px;float:left;'>
						<h4>Напоминание о важном</h4>						
						<p>Получайте рекомендации, созданные специально для вас. <br>
Система, персонально настроенная под ваши требования, <br>автоматически напомнит о необходимости выполнить рекомендации <br>медицинского специалиста: принять препарат или выполнить измерения.</p>						
					</div>
					
				</div>
				<!-- <div class="screen4-block-list-right">
					<img src="./img/screen4.png" alt="">
				</div> -->
			</div>
		</div>
	</div>
</template>
<script>
	export default{

	}
</script>
<style>
h2{
	margin:0;	
	font-size: 30px;
	color:#31496b;
	padding-top:95px;
}
	#screen4{
		width:100vw;
		height:auto;
		background-color:#fafaff;
		position:relative;
	}
	.screen4-block-list-right img{
		position:absolute;
		top:-35%;
		width:100%;
	}
	.screen4-block{
	}
	.screen4-block-title{		
		text-align:center;
	}
	.screen4-block-list{
		background-image:url(/assets/app/build/zdoroviya_dnevnik_msk/screen4.png);
		background-position: center;
		background-repeat: no-repeat;
		background-size:cover;
		padding:70px;
		color:#60759d;
	}
	.screen4-block-list-left{
		display:grid;
		grid-template-columns:repeat(2,1fr);
		padding:40px;
	}
	.screen4-block-list-left p{
		display:table;
		line-height: 24px;
	}
		@media (min-width: 250px) and (max-width: 800px){
			.screen4-block-list{
				padding:5px;
				margin:unset;
			}
			.screen4-block-list-left{
				display:block;
				padding:unset;
			}
		}
</style>