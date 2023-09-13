<script>
	import Header from '../lib/components/Header.svelte';
	import Footer from '../lib/components/footer.svelte';
	import '../lib/normalize.css';
	import '../lib/styles.css';
</script>

<div class="app">
	<Header />

	<main>
		<slot />
	</main>

	<Footer />
</div>

<style>

</style>
