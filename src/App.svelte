<script>
	import Router from 'svelte-spa-router'
	export let name;
	const routes = new Map();
</script>

<main>
	<h1>Hello {name}!</h1>
	<Router {routes} />
</main>

<style>

</style>