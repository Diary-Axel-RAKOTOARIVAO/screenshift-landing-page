<script lang="ts">
	import Footer from '$lib/layout/footer.svelte';
	import Header from '$lib/layout/header.svelte';
	import '../app.css';
	import '../scss/global.scss';
	import '@fontsource-variable/inter';

	let { children } = $props();
</script>

<main>
	<Header />
	{@render children()}
	<Footer />
</main>
