<script>
	// @ts-nocheck
	import Card from './Card.svelte';

	let count = 0;

	function incrementCount() {
		count += 1;
	}
</script>

<Card>
	<button on:click={incrementCount}>
		Clicked {count}
		{count === 1 ? 'time' : 'times'}
	</button>
</Card>
