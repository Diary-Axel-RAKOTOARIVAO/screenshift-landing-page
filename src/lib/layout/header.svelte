<script>
	import 'iconify-icon';
</script>

<header>
	<nav data-screenshift>
		<a class="logo" href="/">Screenshift</a>
		<div class="actions">
			<a href="/" aria-label="Redirecting to Screenshift Github repo">
				<iconify-icon icon="akar-icons:github-fill"></iconify-icon>
			</a>
			<label class="swap swap-rotate">
				<!-- this hidden checkbox controls the state -->
				<input type="checkbox" />

				<!-- sun icon -->
				<iconify-icon icon="solar:sun-bold" class="swap-on"></iconify-icon>
				<iconify-icon icon="solar:moon-bold" class="swap-off"></iconify-icon>
			</label>
		</div>
	</nav>
</header>

<style>
	iconify-icon {
		font-size: 1.75rem;
	}
</style>
