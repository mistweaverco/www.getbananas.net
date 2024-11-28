<script>
	import '$lib/index/fonts.css';
	import '@fortawesome/fontawesome-free/css/all.min.css';
	import './page.css';
</script>

<div class="app">
	<main>
		<slot />
	</main>
</div>

<style>
	.app {
		display: block;
		flex-direction: column;
		height: auto;
		min-height: 100vh;
	}
</style>
