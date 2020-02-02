<script>
  import { onMount } from "svelte";
  import Continent from "./Continent.svelte";
  import Continents from "./Continents.svelte";

  let continents;
  let continent;

</script>

<svelte:head>
  <title>Svelte Continent App</title>
</svelte:head>

<style>

main {
  background-color: lavenderblush;
  font-size: 15px;
}
  h1 {
    font-size: 25px;
	}

</style>

  <h1>The Seven Continents Svelte App</h1>
<main>
		<Continents {continents} />
</main>