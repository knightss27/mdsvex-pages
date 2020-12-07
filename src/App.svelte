<script>
	import Router from 'svelte-spa-router'
	const routes = new Map();
	import MDPNavbar from 'rollup-plugin-mdsvex-pages/src/MDPNavbar.svelte'
</script>

<!-- <MDPNavbar {routes} /> -->

<main>
	<Router {routes} />
</main>

<style>
	main {
		padding-bottom: 10000px;
	}
</style>