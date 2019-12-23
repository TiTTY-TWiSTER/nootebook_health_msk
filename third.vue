<template>
	<div id="screen3">
		<div class="container-main" style="color:#60759d;">
			<p style="padding-top:6rem;">Функции приложения</p>
		</div>
		<div class="info-graph">
			<div class="row">
				<div class="row-item">
					<img src="/assets/app/build/zdoroviya_dnevnik_msk/icon1.png" alt="">
					<p>Планирование графика <br> приема лекарств</p>
				</div>
				<div class="row-item">
					<img src="/assets/app/build/zdoroviya_dnevnik_msk/icon2.png" alt="">
					<p>Уведомление врача <br> об исполнении назначений</p>
				</div>
				<div class="row-item">
					<img src="/assets/app/build/zdoroviya_dnevnik_msk/icon3.png" alt="">
					<p>Ведение дневника <br> самочувствия</p>
				</div>
			</div>
			<div class="row">
				<div class="row-item">
					<img src="/assets/app/build/zdoroviya_dnevnik_msk/icon4.png" alt="">
					<p>Удаленное предоставление <br> измерений врачу</p>
				</div>
				<div class="row-item">
					<img src="/assets/app/build/zdoroviya_dnevnik_msk/icon5.png" alt="">
					<p>Общение с врачами <br> через встроенный мессенджер</p>
				</div>
				<div class="row-item">
					<img src="/assets/app/build/zdoroviya_dnevnik_msk/icon6.png" alt="">
					<p>Получение уведомлений <br> для выполнения назначений</p>
				</div>
			</div>
		</div>
	</div>
</template>
<script>
	export default{

	}
</script>
<style>
	#screen3{
		text-align: center;
		width:100vw;
		position:relative;
		background-image: url(/assets/app/build/zdoroviya_dnevnik_msk/screen3-bg.png);
		-webkit-background-size: cover;background-size: cover;
		background-repeat:no-repeat;
		margin-top:-62px;
		color:#60759d;
	}
	.info-graph{
		padding:10px;
	}
	.row{
		margin:30px;
		display:grid;
		grid-template-columns: repeat(3,1fr);
	}
	.row p{
		font-size: 16px;
		line-height: 24px;
	}
	@media (min-width: 250px) and (max-width: 1000px){
		#screen3{
			width:unset;
			height:unset;
			background-size:cover;
		}
		.row{
			grid-template-columns: repeat(1,1fr);
		}
	}
</style>