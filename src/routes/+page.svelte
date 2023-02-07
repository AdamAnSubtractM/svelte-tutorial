<script>
	// @ts-nocheck
	import Card from '../components/Card.svelte';
	let src = '/image.gif';
</script>

<h1>Adam's Svelte Tutorial</h1>
<Card />
<Card {src}
	>This text is slot content! Similar to React's `children` prop. This instance of card also has a
	src prop passed to it. That src prop renders this image below:
</Card>

<style>
	@import 'sanitize.css';
	:root {
		font-family: system-ui, -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu,
			Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
		padding: 2rem;
	}
</style>
