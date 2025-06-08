<script>
	import 'iconify-icon';
	const packageManager = [
		{
			id: 1,
			icon: 'devicon:bun',
			prefix: 'bun',
			command: 'bun add -D screenshift'
		},
		{
			id: 2,
			icon: 'devicon:npm',
			prefix: 'npm',
			command: 'npm i -D screenshift'
		},
		{
			id: 3,
			icon: 'logos:deno',
			prefix: 'deno',
			command: 'deno i -D npm:screenshift'
		},
		{
			id: 4,
			icon: 'devicon:pnpm',
			prefix: 'pnpm',
			command: 'pnpm add -D screenshift'
		},
		{
			id: 5,
			icon: 'devicon:yarn',
			prefix: 'yarn',
			command: 'yarn add -D screenshift'
		}
	];
</script>

<div class="install">
	<p>1. Just install it with your favorite Package Manager</p>
	<div class="tabs tabs-lift">
		{#each packageManager as item (item.id)}
			<label class="tab">
				<input
					type="radio"
					name="choose_package_manager"
					checked={item.prefix === 'bun' ? true : false}
				/>
				<iconify-icon icon={item.icon}></iconify-icon>
				{item.prefix}
			</label>
			<div class="tab-content bg-base-300 p-6">{item.command}</div>
		{/each}
	</div>
</div>

<style>
	label {
		gap: 6px;
	}
</style>
