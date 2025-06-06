<script lang="ts">
	let status: '' | 'debug' = $state('');
	function debugMode() {
		status = status === '' ? 'debug' : '';
	}
</script>

<section id="toggle">
	<div class="content" data-screenshift={status}>
		{#if !status}
			<h3>Wanna see something great ?</h3>
			<h4>Click the button</h4>
		{:else}
			<h3>Now try to resize your window</h3>
			<h4>And see how the overlay tells you which breakpoints aliases to use</h4>
		{/if}
		<button onclick={debugMode} class="btn btn-primary">
			{#if !status}
				Debug Mode
			{:else}
				Normal Mode
			{/if}
		</button>
	</div>
</section>
