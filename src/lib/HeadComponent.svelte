<script>
	export let data;
</script>

<svelte:head>
	<title>{data.title}</title>
	<meta name="description" content={data.description} />
	<style>
		@import '$lib/styles.css';
	</style>
</svelte:head>
