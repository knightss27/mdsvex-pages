<script>
	import Router from 'svelte-spa-router'
	const routes = new Map();
</script>

<main>
	<Router {routes} />
</main>

<style>
	main {
		padding-bottom: 10000px;
	}
</style>