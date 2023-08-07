<script>
	import '../app.css';

	import { fly } from 'svelte/transition';
	import Nav from '../components/Nav.svelte';

	export let data;
</script>

<div class="app">
	<Nav />
	<main>
		{#key data.url}
			<div in:fly={{ x: 300, duration: 300, delay: 300 }} out:fly={{ x: -300, duration: 300 }}>
				<slot />
			</div>
		{/key}
	</main>
</div>

<style>
</style>
