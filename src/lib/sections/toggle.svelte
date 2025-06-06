<script lang="ts">
	let status: '' | 'debug' = $state('');
	function debugMode() {
		status = status === '' ? 'debug' : '';
	}
</script>

<section id="toggle">
	<div class="content" data-screenshift={status}>
		<h3>Wanna see something great ?</h3>
		<h4>Click the button</h4>
		<button onclick={debugMode} class="btn btn-primary">Debug Mode</button>
	</div>
</section>
