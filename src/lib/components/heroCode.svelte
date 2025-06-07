<script>
	import { Carta, Markdown } from 'carta-md';
	import { code } from '@cartamd/plugin-code';
	import DOMPurify from 'isomorphic-dompurify';
	import '@cartamd/plugin-code/default.css';
	const carta = new Carta({
		sanitizer: DOMPurify.sanitize,
		extensions: [
			code({
				theme: 'github-dark',
				langs: ['scss']
			})
		],
		shikiOptions: {
			themes: ['github-dark']
		}
	});
	let value = `
\`\`\`scss

@use 'screenshift/scss' as *;

.card {
  display: flex;
  gap: 2rem;

  // For desktop and below
  @include max-mq("desktop") {
    gap: 1.5rem;
  }

  // For tablets and below
  @include max-mq("tablet") {
    flex-direction: column;
    gap: 1rem;
  }

  // For mobile
  @include max-mq("mobile") {
    padding: 1rem;
    background-color: #fef3c7;
  }
}
`;
	let htmlTemplate = `
\`\`\`html
<div class="your-container" data-screenshift>
   <!--- Your content --->
  </div>
`;
</script>

<div class="mockup-code">
	<Markdown {carta} {value} />
</div>

<style>
	:global(.shiki) {
		background: none !important;
	}
	:global(.mockup-code pre) {
		padding: 0 16px;
	}
</style>
