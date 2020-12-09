<script>
	import Router from 'svelte-spa-router'
	const routes = new Map();
	import MDPWrapper from 'rollup-plugin-mdsvex-pages/src/components/MDPWrapper.svelte'
</script>

<MDPWrapper styles={{}}>
	<main>
		<Router {routes} />
	</main>
</MDPWrapper>


<style>
	/* main {
		padding-bottom: 10000px;
	} */
</style>
