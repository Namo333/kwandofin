<script>
	import { onMount } from 'svelte';

	import Wrapper from "../lib/components/wrapper.svelte";
	import Calculate from "../lib/components/calculate.svelte";
	import Portslider from "../lib/components/slider.svelte";
	import famBg from "../lib/img/famyli.svg";
	import artimg from '../lib/img/art.svg';

	// onMount(() => {
    //     const slider = document.querySelector('.fixed-slider');
        
    //     window.addEventListener('scroll', () => {
    //         const rect = slider.getBoundingClientRect();
    //         const isInViewport = rect.top >= 0 && rect.bottom <= window.innerHeight;
            
    //         if (isInViewport) {
    //         slider.classList.add('fixed');
    //         } else {
    //         slider.classList.remove('fixed');
    //         }
    //     });
        
    //     slider.addEventListener('wheel', (event) => {
    //         event.preventDefault(); // Отменяем стандартное поведение прокрутки страницы
            
    //         const delta = Math.sign(event.deltaY); // Получаем направление прокрутки
            
    //         if (delta > 0) {
    //         // Прокрутка вниз, переключаемся на следующий слайд
    //         // Добавьте здесь свой код для переключения на следующий слайд
    //         } else if (delta < 0) {
    //         // Прокрутка вверх, переключаемся на предыдущий слайд
    //         // Добавьте здесь свой код для переключения на предыдущий слайд
    //         }
    //     });
    // });
</script>

<svelte:head>
	<title>Home</title>
	<meta name="description" content="Svelte demo app" />
</svelte:head>

<section class="herro">
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
				<img class="hero__rightImg" src="{ famBg }" alt="">
			</div>
		</div>
	</Wrapper>
</section>

<section class="content__info">
	<Wrapper>
		<div class="content__infoBlock">
			<div class="infoBlock__one">
				<img src="{ artimg }" alt="">
				<div class="infoBlock__oneItem">
					<h1 class="oneItem__title">Simple and Fast Cryptocurrency
						Payment System.</h1>
					<p class="oneItem__text">Integrate Crypto Pay into your Telegram bot or website to provide your users with convenient and reliable cryptocurrency payment options. Our system ensures security, speed, and ease of use to meet your business needs.</p>
				</div>
			</div>
			<div class="infoBlock__set">
				<div class="infoBlock__left">
					<svg width="48" height="48" viewBox="0 0 48 48" fill="none" xmlns="http://www.w3.org/2000/svg">
						<path d="M14 16L6 24L14 32" stroke="#41A4DF" stroke-width="3" stroke-linecap="round" stroke-linejoin="round"/>
						<path d="M34 16L42 24L34 32" stroke="#41A4DF" stroke-width="3" stroke-linecap="round" stroke-linejoin="round"/>
						<path d="M28 8L20 40" stroke="#41A4DF" stroke-width="3" stroke-linecap="round" stroke-linejoin="round"/>
					</svg>
					<h1 class="infoBlock__leftTitle">Invoicing and Payment Verification via API</h1>
					<p class="infoBlock__leftText">Create invoices in @CryptoBot and allow users to instantly and securely pay them using the API.</p>
				</div>
				<div class="infoBlock__right">
					<svg width="48" height="48" viewBox="0 0 48 48" fill="none" xmlns="http://www.w3.org/2000/svg">
						<path d="M14 16L6 24L14 32" stroke="#41A4DF" stroke-width="3" stroke-linecap="round" stroke-linejoin="round"/>
						<path d="M34 16L42 24L34 32" stroke="#41A4DF" stroke-width="3" stroke-linecap="round" stroke-linejoin="round"/>
						<path d="M28 8L20 40" stroke="#41A4DF" stroke-width="3" stroke-linecap="round" stroke-linejoin="round"/>
					</svg>
					<h1 class="infoBlock__leftTitle">Convenient Usage Statistics</h1>
					<p class="infoBlock__leftText">View the number of created and paid invoices, total number of users, and the percentage of successful payments through our comprehensive usage statistics.</p>
					
				</div>
			</div>
			<div class="infoBlock__thrio">
				<div class="infoBlock__left">
					<svg width="48" height="48" viewBox="0 0 48 48" fill="none" xmlns="http://www.w3.org/2000/svg">
						<path d="M6 16C6 14.4087 6.63214 12.8826 7.75736 11.7574C8.88258 10.6321 10.4087 10 12 10H36C37.5913 10 39.1174 10.6321 40.2426 11.7574C41.3679 12.8826 42 14.4087 42 16V32C42 33.5913 41.3679 35.1174 40.2426 36.2426C39.1174 37.3679 37.5913 38 36 38H12C10.4087 38 8.88258 37.3679 7.75736 36.2426C6.63214 35.1174 6 33.5913 6 32V16Z" stroke="#41A4DF" stroke-width="3" stroke-linecap="round" stroke-linejoin="round"/>
						<path d="M6 20H42" stroke="#41A4DF" stroke-width="3" stroke-linecap="round" stroke-linejoin="round"/>
						<path d="M14 30H14.02" stroke="#41A4DF" stroke-width="3" stroke-linecap="round" stroke-linejoin="round"/>
						<path d="M22 30H26" stroke="#41A4DF" stroke-width="3" stroke-linecap="round" stroke-linejoin="round"/>
					</svg> 
					<h1 class="infoBlock__leftTitle">Balance top-up, payment for goods and services</h1>
					<p class="infoBlock__leftText">Crypto Pay allows you to organize balance top-up, payment for goods, services, or subscriptions through the system.</p>
				</div>
				<div class="infoBlock__left">
					<svg width="48" height="48" viewBox="0 0 48 48" fill="none" xmlns="http://www.w3.org/2000/svg">
						<path d="M23.9997 6C28.6713 10.1332 34.7686 12.2851 40.9997 12C41.9069 15.086 42.1844 18.3229 41.8159 21.5184C41.4474 24.7138 40.4403 27.8025 38.8545 30.6011C37.2686 33.3996 35.1364 35.8508 32.5846 37.809C30.0327 39.7672 27.1132 41.1924 23.9997 42C20.8861 41.1924 17.9666 39.7672 15.4148 37.809C12.8629 35.8508 10.7307 33.3996 9.14486 30.6011C7.55903 27.8025 6.55194 24.7138 6.18342 21.5184C5.8149 18.3229 6.09248 15.086 6.99967 12C13.2307 12.2851 19.328 10.1332 23.9997 6Z" stroke="#41A4DF" stroke-width="3" stroke-linecap="round" stroke-linejoin="round"/>
					</svg> 
					<h1 class="infoBlock__leftTitle">Access Restriction
						and Control</h1>
					<p class="infoBlock__leftText">Configure API access for specific IP addresses and manage them.</p>
				</div>

				<div class="infoBlock__left blue">
					<svg class="blueImg" width="46" height="48" viewBox="0 0 46 48" fill="none" xmlns="http://www.w3.org/2000/svg">
						<path d="M0.993361 14.2681L12.3788 35.0749C12.9425 36.3054 14.7461 36.1935 15.6479 34.5156L22.9752 21.0918C21.7352 18.8173 19.1199 14.0444 18.5788 13.1495C18.0377 12.2545 17.0758 11.9562 16.6624 11.9189H2.34608C0.542469 11.9189 0.655198 13.5969 0.993361 14.2681Z" fill="#BEE5F7"/>
						<path d="M30.0768 11.9184H43.8295C45.3626 11.9184 45.4995 13.4845 45.0695 14.2675C41.6501 20.4947 34.7437 33.1726 34.0222 34.515C33.3008 35.8574 32.1434 36.193 31.655 36.193H14.7459C13.7539 36.193 12.9423 35.7828 12.7168 35.5218C14.1597 36.4167 15.3095 35.1862 15.6477 34.515C18.804 28.698 25.5114 16.5139 26.8077 14.1557C28.1604 11.6947 29.4004 11.9184 30.0768 11.9184Z" fill="white"/>
					</svg> 
					<h1 class="infoBlock__leftTitle blueText">The API allows creating invoices that users can instantly pay</h1>
					<a href="" class="infoBlock__leftButton">
						Оставить заявку 
						<svg width="25" height="24" viewBox="0 0 25 24" fill="none" xmlns="http://www.w3.org/2000/svg">
							<path d="M17.4497 7.05026L7.55024 16.9498M17.4497 7.05026V15.5355M17.4497 7.05026H8.96445" stroke="white" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/>
						</svg> 
					</a>
				</div>
				
			</div>
		</div>
	</Wrapper>
</section>

<section class="colculate">
	<Wrapper>
		<div class="colculate__block">
			<div class="colculate__blockLeft">
				<h1 class="colculate__blockLefTitle">The commission for applications ranges from 2.5% to 3%</h1>
				<p class="colculate__blockLeftext">The commission rates are as follows,
					based on the total amount of paid invoices</p>
				<a href="" class="colculate__blockLefButton">
					Рассчитайте кредит
					<svg width="25" height="24" viewBox="0 0 25 24" fill="none" xmlns="http://www.w3.org/2000/svg">
						<path d="M19.4999 12L5.49994 12M19.4999 12L13.4999 18M19.4999 12L13.4999 6" stroke="white" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/>
					</svg> 
				</a>
			</div>
			<div class="colculate__blockRight">
				<Calculate />
			</div>
		</div>
	</Wrapper>
</section>

<section>
    <Wrapper>

    </Wrapper>
</section>

<section class="part__block fixed-slider">
    <Wrapper>
		<div class="part__blockContent">
			<Portslider />
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
		max-width: calc(100% -  985px );
		flex-shrink: 0; 
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

	.infoBlock__one{
		display: flex;
		align-items: center;
		justify-content: center;
		background: #FAFAFA;
		border-radius: 36px;
		padding: 48px 0 48px 0; 
	}

	.infoBlock__set{
		display: flex;
		justify-content: space-between;
	}

	.content__infoBlock{
		max-width: 100vh;
		margin: 0 auto;
	}

	.infoBlock__right{
		margin-left: 100px;
	}

	.oneItem__title{
		font-size: 48px;
		font-style: normal;
		font-weight: 700;
		line-height: normal;
		letter-spacing: -0.96px; 
	}
	.oneItem__text{
		font-size: 20px;
		font-style: normal;
		font-weight: 400;
		line-height: 180%; /* 36px */ 
		color: var(--color-smol-text);
	}

	.infoBlock__oneItem{
		margin-left: 40px;
	}

	.infoBlock__left{
		background: #FAFAFA;
		border-radius: 36px;
		padding: 20px 36px; 
	}
	.infoBlock__right{
		background: #FAFAFA;
		border-radius: 36px;
		padding: 20px 36px; 
	}

	.infoBlock__leftTitle{
		font-size: 24px;
		font-style: normal;
		font-weight: 600;
		line-height: 140%; /* 33.6px */
		letter-spacing: 0.12px;
	}

	.infoBlock__leftText{
		font-size: 16px;
		font-style: normal;
		font-weight: 400;
		line-height: 180%; /* 28.8px */
		letter-spacing: 0.4px;
		color: var(--color-smol-text);
	}

	.infoBlock__thrio{
		display: flex;
		gap: 60px;
	}

	.blue{
		border-radius: 36px;
		background-color: var(--color-main);
		display: flex;
		padding: 48px 36px;
		flex-direction: column;
		justify-content: space-between;
		align-items: center;
		align-self: stretch;
	}

	.blueText{
		text-align: center;
		color: var(--color-text2);
		font-size: 24px;
		font-style: normal;
		font-weight: 700;
		line-height: normal;
		letter-spacing: -0.48px; 
	}

	.infoBlock__leftButton{
		color: #fff;
		align-items: center;
		display: flex;
	}

	.colculate{
		background: var(--color-dark-bg);
		padding: 100px 0;
	}

	.colculate__block{
		display: flex;
		align-items: center;
		align-content: center;
		justify-content: center;
	}

	.colculate__blockLeft{
		color: #fff;
		margin-right: 171px;
	}

	.colculate__blockLefTitle{
		font-size: 48px;
		font-style: normal;
		font-weight: 700;
		line-height: normal;
		letter-spacing: -0.96px; 
	}

	.colculate__blockLeftext{
		color: #B3B3B3;
		font-size: 20px;
		font-style: normal;
		font-weight: 400;
		line-height: 180%; /* 36px */ 
	}

	.colculate__blockLefButton{
		color: #fff;
		background: #41A4DF;
		border-radius: 36px;
		flex-shrink: 0;
		display: flex;
		width: 246px;
		height: 22px; 
		padding: 12px 12px 12px 24px; 
		justify-content: center;
		align-items: center;
		gap: 8px; 
	}

	.part__block{
		background: #232328; 
	}
	/* .fixed-slider{
		height: 100vh;  
    	overflow-y: scroll;   
		overflow: hidden;
	}*/



</style>
