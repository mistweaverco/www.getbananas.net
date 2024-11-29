<script>
	export let data;
</script>

<svelte:head>
	<title>{data.title}</title>
	<meta name="description" content={data.description} />
	<meta property="og:image" content="/open-graph.png" />
	<style>
		@import '$lib/styles.css';
	</style>
</svelte:head>
