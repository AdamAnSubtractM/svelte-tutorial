<script>
	/**
	 * @type {?string}
	 */
	export let title;
	/**
	 * @type {?string}
	 */
	export let src;
</script>

<section>
	{#if title}
		<h2>{title}</h2>
	{:else}
		<h2>Card Component</h2>
	{/if}

	<p>
		Testing out this card component. Styles defined in this component are scoped to it regardless of
		the tag/class selector used.
	</p>
	<slot />
	{#if src}
		<img {src} alt="Never gonna give you up, never gonna let you down!" />
	{/if}
</section>

<style>
	section {
		--round: 2rem;
		border: 1px solid lightgray;
		border-radius: var(--round);
		padding: 2rem;
		margin: 1rem 0;
		max-width: 400px;
		width: 100%;
	}
	h2 {
		margin-top: 0;
	}
	img {
		width: 100%;
		border-radius: calc(var(--round) / 2);
		margin: 1rem 0;
	}
</style>
