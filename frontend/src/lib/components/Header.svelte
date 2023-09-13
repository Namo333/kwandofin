<script>
	import { page } from '$app/stores';
	import logo from '../img/logo.svg';
</script>

<header>
	<div class="wrapper">
		<li aria-current={$page.url.pathname === '/' ? 'page' : undefined}>
			<a href="/" class="header__logo"><img class="header__logoImg" src="{ logo }" alt=""> квандо финанс</a>
		</li>
		
		<nav class="header__navigarion">
			<ul class="navigarion__list">
				<li class="navigarion__item" aria-current={$page.url.pathname === '/about' ? 'page' : undefined}>
					<a class="navigarion__link" href="/about">Услуги</a>
				</li>
				<li class="navigarion__item" aria-current={$page.url.pathname.startsWith('/sverdle') ? 'page' : undefined}>
					<a class="navigarion__link" href="/sverdle">О компании</a>
				</li>
				<li class="navigarion__item" aria-current={$page.url.pathname.startsWith('/sverdle') ? 'page' : undefined}>
					<a class="navigarion__link" href="/sverdle">Отзывы</a>
				</li>
				<li class="navigarion__item" aria-current={$page.url.pathname.startsWith('/sverdle') ? 'page' : undefined}>
					<a class="navigarion__link" href="/sverdle">Новости</a>
				</li>
				<li class="navigarion__item" aria-current={$page.url.pathname.startsWith('/sverdle') ? 'page' : undefined}>
					<a class="navigarion__link" href="/sverdle">Контакты</a>
				</li>
			</ul>
		</nav>
	</div>
</header>

<style>
	header{
		width: 100%;
		height: 70px;
	}

	header .wrapper{
		height: inherit;
		display: flex;
		justify-content: space-between;
		max-width: 1980px;
		margin: 0 auto;
		padding: 24px 140px;
	}

	.header__logo{
		text-decoration: none;
		display: flex;
		align-items: center;
		color: var(--color-main);
		font-size: 30px;
		font-style: normal;
		font-weight: 700;
		line-height: normal; 
	}

	.header__logoImg{
		margin-right: 6px;
	}

	.navigarion__list{
		display: flex;
		gap: 54px;
	}
</style>
