<script>
	// @ts-nocheck
	import Card from './Card.svelte';
	let numbers = [1, 2, 3, 4];

	// won't work!
	function addNumber() {
		numbers.push(numbers.length + 1);
		// will cause this to work:
		// numbers = numbers;
	}

	// But this is an even better option:
	// function addNumber() {
	// 	numbers = [...numbers, numbers.length + 1];
	// }

	$: sum = numbers.reduce((t, n) => t + n, 0);
</script>

<Card title="How do we fix this counter's reactivity?">
	<p>{numbers.join(' + ')} = {sum}</p>

	<button on:click={addNumber}> Add a number </button>
</Card>
