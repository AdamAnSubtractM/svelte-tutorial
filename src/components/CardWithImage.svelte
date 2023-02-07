<script>
	/**
	 * @type {any}
	 */
	export let children;
	/**
	 * @type {string}
	 */
	export let src;
</script>

<section>
	<h2>Card Component</h2>
	{#if children}
		<p>
			{children}
		</p>
	{/if}
	{#if src}
		<img {src} alt="Never gonna give you up, never gonna let you down!" />
	{/if}
</section>

<style>
	section {
		border: 1px solid lightgray;
		border-radius: 2rem;
		padding: 2rem;
		max-width: 300px;
	}
	h2 {
		margin-top: 0;
	}
</style>
