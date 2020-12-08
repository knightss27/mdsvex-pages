<script>
	import Router from 'svelte-spa-router'
	const routes = new Map();
	import MDPWrapper from 'rollup-plugin-mdsvex-pages/src/MDPWrapper.svelte'
</script>

<MDPWrapper>
	<main>
		<Router {routes} />
	</main>
</MDPWrapper>


<style>
	main {
		padding-bottom: 10000px;
	}
</style>