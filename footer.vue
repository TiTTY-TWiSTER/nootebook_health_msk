<template>
	<div id="footer">
		<div class="footer-nav">
			<div>
				<img src="/assets/app/build/zdoroviya_dnevnik_msk/footer-logo.png" alt="" style="margin-right:80px;">
			</div>
			<p>О сервисе</p>
			<p>Функции</p>
			<p>Возможности</p>
			<p>Специалистам</p>
			<a href="tel:+79996694737" style="text-decoration:none;color:white;">
				<span>+7(999) 669-47-37</span>
			</a>
		</div>
		
	</div>
</template>
<script>
	export default{

	}
</script>
<style>
	#footer{
		position:relative;
		height: auto;
		background-color: #39649d;
		padding:65px;
		color:white;		
	}
	.footer-nav{
		display:flex;
		justify-content: space-between;
		align-items:center;
		border-bottom:1px solid #335b91;
		padding-bottom:55px;	
	}
	.footer-nav p{
		cursor:pointer;
		margin:unset;
		padding:unset;
	}
	@media (min-width: 250px) and (max-width: 800px){
		.footer-nav{
			display:block;
		}
	}
	</style>