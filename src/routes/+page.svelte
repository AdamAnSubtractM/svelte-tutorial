<script>
	// @ts-nocheck
	import AddNumberCounter from '../components/AddNumberCounter.svelte';
	import ButtonIncrementer from '../components/ButtonIncrementer.svelte';
	import Card from '../components/Card.svelte';
	import HtmlComponent from '../components/HTMLComponent.svelte';
	import ReactiveCounter from '../components/ReactiveCounter.svelte';
	let src = '/image.gif';
	let name = 'Adam';
</script>

<h1>{name}'s Svelte Tutorial</h1>
<div class="container">
	<Card />
	<Card {src}
		>This text is slot content! Similar to React's `children` prop. This instance of card also has a
		src prop passed to it. That src prop renders this image below:
	</Card>
	<ButtonIncrementer />
	<HtmlComponent />
	<ReactiveCounter />
	<AddNumberCounter />
</div>

<style>
	@import 'sanitize.css';
	:root {
		--gap: 2rem;
		font-family: system-ui, -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu,
			Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
		padding: var(--gap);
	}

	.container {
		display: flex;
		justify-content: space-between;
		flex-flow: row wrap;
		gap: var(--gap);
	}
</style>
