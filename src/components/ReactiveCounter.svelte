<script>
	// @ts-nocheck

	import Card from './Card.svelte';

	let count = 0;

	$: if (count >= 10) {
		alert('count is dangerously high!');
		count = 9;
	}

	$: {
		console.log('the count is ' + count);
	}

	function handleClick() {
		count += 1;
	}
</script>

<Card title={'Reactive Counter'}>
	<button on:click={handleClick}>
		Clicked {count}
		{count === 1 ? 'time' : 'times'}
	</button>
</Card>
