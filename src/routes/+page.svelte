<script>
	let num = 57;

	function increment() {
		num += 1;
	}
</script>

<svelte:head>
	<title>Home</title>
	<meta name="description" content="Svelte demo app" />
</svelte:head>

<section>
	<p>The number is {num}</p>
	<button on:click={increment}>Click me</button>

	{#if num === 60}
		<p>You found the magic number!</p>
	{:else}
		<p>Keep clicking until you find the magic number</p>
	{/if}
</section>

<style>
	section {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		flex: 0.6;
	}
</style>
