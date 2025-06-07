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
\`\`\`css
.testing {
	background: red;
	color: white;
	padding: 10px;
	border-radius: 5px;
}
`;
</script>

<div class="mockup-code">
	<Markdown {carta} {value} />
</div>

<style>
	:global(.shiki) {
		background: none !important;
	}
</style>
