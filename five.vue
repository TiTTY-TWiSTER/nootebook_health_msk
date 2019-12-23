<template>
	<div id="screen5">
		<img src="/assets/app/build/zdoroviya_dnevnik_msk/planshet.png" alt="">
		<div class="screen5-text-block">
			<h2>Специалистам</h2>
			<ul>
				<li>
					<p>Дистанционный контроль состояния здоровья ваших пациентов</p>
				</li>
				<li>
					<p>Наблюдение за динамикой изменения основных <br> медицинских показателей </p>
				</li>
				<li>
					<p>Наличие алгоритмов автоматического анализа <br> поступающей информации</p>
				</li>
				<li>
					<p>Индивидуальная система уведомлений об изменении <br> состояния каждого пациента</p>
				</li>
				<li>
					<p>Дополнительный сервис коммуникации, позволяющий активно <br> вовлекать пациента в процесс профилактики, лечения и реабилитации.</p>
				</li>
			</ul>
		</div>
	</div>
</template>
<script>
	export default{

	}
</script>
<style>
	#screen5{
		width:100vw;
		height: 65vh;
		position:relative;
		background-color:#f1f2fa;
	}
	#screen5 img{
		width:47%;
		margin-top:-5rem;
	}
	.screen5-text-block{
		position:absolute;
		right:2%;
		top:0;
	}
	.screen5-text-block h2{
		color:#60759d;
	}
	.screen5-text-block ul{
		display:block;
		color:#16afe0;
		padding:15px;
	}
	.screen5-text-block p{
		color:#60759d;
	}

	@media (min-width: 250px) and (max-width: 800px){
		#screen5{
			height:auto;
		}
		.screen5-text-block{
			position:unset;
			display:block;
			padding:15px;
			margin-top: -4rem;
		}
		#screen5 img{
			width:100%;
			margin-top:unset;			
		}		
	}
</style>