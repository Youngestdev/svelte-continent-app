<script>
	export let continent;
</script>

<style>
	article {
		margin: 0 0 1em 0;
	}

	h1 {
		font-size: 1.4em;
		margin: 0;
		display: block;
	}
</style>

<article>
		<h1>{continent.name}</h1>
		<small>
			Population: <b>{continent.population}</b>		
		</small><br/>
		<small>
			Number of countries: <b>{continent.no_of_countries}</b>
		</small><br/>
		<small>
			Continent's size: <b>{continent.area}</b>
		</small>
</article>