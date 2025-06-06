<script>
	import html from '$lib/assets/images/syntax/html.webp';
	import scss from '$lib/assets/images/syntax/scss.webp';
</script>

<section id="syntax">
	<div class="content" data-screenshift>
		<div class="title">
			<h3>Introducing a new syntax</h3>
			<h4>Cleaner code, less hastle</h4>
		</div>
		<div class="illustration">
			<div class="html">
				<p>Drop it on any container — that’s it.</p>
				<img src={html} alt="" />
				<p>
					It auto-applies responsive padding, max-widths, and margin rules based on screen size. No
					need to write boilerplate container styles.
				</p>
			</div>
			<div class="scss">
				<p>Forget writing verbose media queries.</p>
				<img src={scss} alt="" />
				<p>
					Cleaner, more readable, and easier to maintain. And yes — there’s a min-mq(...) too if you
					prefer mobile-first.
				</p>
			</div>
		</div>
	</div>
</section>
