<script>
	let firstName = 'Ivandi'
	let lastName = 'Djoh Gah'

	$: name = firstName + ' ' + lastName
</script>

<main>
	<h1>Hello, {name}!</h1>
	<!-- 
	{#if !age}
		<p>I'm not <strong>{age -1}</strong> years old right now.</p>
	{:else}
		<p>I'm <strong>{age}</strong> years old right now.</p>
	{/if} -->
</main>

<style>
	main {
		text-align: center;
		padding: 1em;
		max-width: 240px;
		margin: 0 auto;
	}

	h1 {
		color: rgb(17, 15, 128);
		text-transform: uppercase;
		font-size: 4em;
		font-weight: 100;
	}

	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
</style>