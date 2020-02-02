<script>
	import { onMount } from "svelte";
	import Continent from "./Continent.svelte";

	let continents;

	onMount(async () => {
		await fetch(`http://localhost:8081/`)
			.then(r => r.json())
			.then(data => {
				continents = data;
			});
	})


</script>

<style>
	.loading {
		opacity: 0;
		animation: 0.4s 0.8s forwards fade-in;
	}

	@keyframes fade-in {
		from { opacity: 0; }
		to { opacity: 1; }
	}

	li {
		list-style-type: georgian;
	}
</style>

{#if continents}
	{#each continents as continent }
		<ul>
			<li>		
				<Continent {continent} />
			</li>
		</ul>
	{/each}

{:else}
	<p class="loading">loading...</p>
{/if}
