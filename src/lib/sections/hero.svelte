<script>
	import CodeBlocks from '$lib/components/codeBlocks.svelte';
</script>

<section id="hero">
	<div class="content" data-screenshift>
		<div class="copy">
			<div class="text">
				<h2>Faster, Cleaner, Less hassle.</h2>
				<h2>Stop wrestling with breakpoints. Just shift.</h2>
			</div>
			<div class="actions"></div>
		</div>
		<div class="illustration">
			<CodeBlocks />
		</div>
	</div>
</section>

<style>
	h2:last-of-type {
		font-weight: 400;
	}
</style>
