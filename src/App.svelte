<script>
	import Router from 'svelte-spa-router'
	const routes = new Map();
</script>

<!-- <nav>Test</nav> -->

<main>
	<Router {routes} />
</main>

<style>
	main {
		padding-bottom: 40000px;
	}

	/* nav {
		width: 100%;
		height: 60px;
		position: sticky;
		top: 0;
		background-color: black;
		color: white;
		z-index: 1500;
	} */
</style>