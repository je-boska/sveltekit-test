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
	<p class="m-8 text-xl">The number is {num}</p>
	<div class="flex gap-2 mb-8 text-2xl">
		<button on:click={() => (num -= 1)} class="py-2 px-4 bg-orange-600 text-white">-</button>
		<button on:click={increment} class="py-2 px-4 bg-blue-700 text-white">+</button>
	</div>

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
