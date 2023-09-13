<script>
	// import Counter from './Counter.svelte';
	// import welcome from '$lib/images/svelte-welcome.webp';
	// import welcome_fallback from '$lib/images/svelte-welcome.png';
	import Wrapper from "../lib/components/wrapper.svelte";
	import famBg from "../lib/img/famyli.svg";
</script>

<svelte:head>
	<title>Home</title>
	<meta name="description" content="Svelte demo app" />
</svelte:head>

<section>
	<Wrapper>
		<div class="content__hero">
			<div class="hero__left">
				<h1 class="hero__leftTitle">
					Банк отказал? мы поможем вам <span class="text__color">ВЗЯТЬ</span> кредит
				</h1>
				<p class="hero__leftText">
					<span class="text__color">Crypto Pay</span> – payment system for the Telegram chat-bots and services developed on top of <span class="text__color">@CryptoBot</span> architecture.
				</p>
				<div class="hero__leftButton">
					<a href="" class="leftButtonLeft">Оставить заявку</a>
					<a href="" class="leftButtonRight">
						Узнать больше 

						<svg width="24" height="24" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
							<path d="M16.2284 11.0081L10.7919 5.68755L12.225 4.28501L20.1081 12L12.225 19.715L10.7919 18.3125L16.2284 12.9919H3.89191V11.0081H16.2284Z" fill="#41A4DF"/>
						</svg> 
					
					</a>
				</div>
				
				<div class="hero__leftInfoContent">
					<div class="leftInfoContent__block">
						<div class="block__item">
							<div class="badge"><span class="badge__ri"><svg width="18" height="18" viewBox="0 0 18 18" fill="none" xmlns="http://www.w3.org/2000/svg">
								<path d="M7.49999 11.379L14.394 4.48425L15.4552 5.54475L7.49999 13.5L2.72699 8.727L3.78749 7.6665L7.49999 11.379Z" fill="white"/>
								</svg> </span></div>
								<p class="block__itemText">
									Ставка от 6.9% годовых
								</p>
						</div>
						<div class="block__item">
							<div class="badge"><span class="badge__ri"><svg width="18" height="18" viewBox="0 0 18 18" fill="none" xmlns="http://www.w3.org/2000/svg">
								<path d="M7.49999 11.379L14.394 4.48425L15.4552 5.54475L7.49999 13.5L2.72699 8.727L3.78749 7.6665L7.49999 11.379Z" fill="white"/>
								</svg> </span></div>
								<p class="block__itemText">
									Без предоплаты
								</p>
						</div>
					</div>

					<div class="leftInfoContent__block">
						<div class="block__item">
							<div class="badge"><span class="badge__ri"><svg width="18" height="18" viewBox="0 0 18 18" fill="none" xmlns="http://www.w3.org/2000/svg">
								<path d="M7.49999 11.379L14.394 4.48425L15.4552 5.54475L7.49999 13.5L2.72699 8.727L3.78749 7.6665L7.49999 11.379Z" fill="white"/>
								</svg> </span></div>
								<p class="block__itemText">
									Быстрое одобрение и получение
								</p>
						</div>
						<div class="block__item">
							<div class="badge"><span class="badge__ri"><svg width="18" height="18" viewBox="0 0 18 18" fill="none" xmlns="http://www.w3.org/2000/svg">
								<path d="M7.49999 11.379L14.394 4.48425L15.4552 5.54475L7.49999 13.5L2.72699 8.727L3.78749 7.6665L7.49999 11.379Z" fill="white"/>
								</svg> </span></div>
								<p class="block__itemText">
									Нужен только паспорт
								</p>
						</div>
					</div>
				</div>
			</div>
			<div class="hero__right">
				<div class="right__bg"></div>
				<img class="hero__rightImg" src="{ famBg }" alt="">
			</div>
		</div>
	</Wrapper>
</section>

<section>
	<Wrapper>
		<div class="content__infoBlock">
			<div class="infoBlock__one">
				
			</div>
		</div>
	</Wrapper>
</section>

<style>

	.text__color{
		color: var(--color-main);
	}
	.content__hero{
		display: flex;
	}

	.hero__left{
		margin: 170px 0;
	}

	.hero__leftTitle{
		max-width: 600px;
		font-feature-settings: 'clig' off, 'liga' off;
		font-size: 43px;
		font-style: normal;
		font-weight: 600;
		line-height: 68px;
		margin: 0;
	}

	.hero__leftText{
		max-width: 700px;
		font-size: 19px;
		font-style: normal;
		font-weight: 500;
		line-height: 170%; 
	}

	.hero__leftButton{
		display: flex;
		align-items: center;
		gap: 32px;
	}

	.leftButtonLeft{
		padding: 16px 24px;
		align-items: center;
		border-radius: 6px;
		background: var(--color-main);
		color: var(--color-text2);
	}

	.leftButtonRight{
		display: flex;
		align-items: center;
		gap: 8px;
		color: var(--color-main);
	}

	.hero__rightImg{
		position: absolute;
		top: 100px; 
		right: 0;
		left: auto;
		width: calc(100% -  985px );
		flex-shrink: 0; 
	}
	

	.right__bg{
		position: absolute;
		top:  0; 
		right: 0;
		left: auto;
		width: calc(100% - 1000px );
		border-radius: 0 0 0 25px;
		height: 102.5vh;
		flex-shrink: 0; 
		background-color: var(--color-bg-main);
		z-index: -1;
	}

	.hero__leftInfoContent{
		display: flex;
	}

	.leftInfoContent__block:nth-child(2){
		margin-left: 80px;
	}

	.badge{
		width: 26px;
		height: 26px;
		display: flex;
		justify-content: center;
		align-items: center;
		background: var(--color-main);
		border-radius: 100px; 
	}

	.badge__ri{
		width: 18px;
		height: 18px;
		flex-shrink: 0; 
	}

	.block__item{
		display: flex;
		align-items: center;
	}

	.block__itemText{
		font-size: 16px;
		font-style: normal;
		font-weight: 500;
		line-height: 180%;
		margin-left: 16px;
	}

</style>
