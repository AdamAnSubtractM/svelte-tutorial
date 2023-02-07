<script>
	// @ts-nocheck
	import Card from './Card.svelte';
	let string = `this string contains some <strong>HTML yo!</strong>`;
</script>

<Card title="Card with HTML rendered in it!">
	<p>{@html string}</p>
</Card>

<style>
	p {
		color: salmon;
	}
</style>
