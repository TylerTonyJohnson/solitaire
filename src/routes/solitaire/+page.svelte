<svelte:head>
	<title>About</title>
	<meta name="description" content="About this app" />
</svelte:head>

<!-- Script -->

<script>
	import Card from './Card.svelte';
</script>

<!-- Structure -->

<main>
	<div id="stock">
		<Card suit='STK'></Card>
	</div>
	<div id="waste">
		<Card suit='WST'></Card>
		<Card suit='WST'></Card>
	</div>
	<div id="foundation">
		<Card suit='FND'></Card>
		<Card suit='FND'></Card>
		<Card suit='FND'></Card>
		<Card suit='FND'></Card>
	</div>
	<div id="tableau">
		<Card suit='TBL'></Card>
		<Card suit='TBL'></Card>
		<Card suit='TBL'></Card>
		<Card suit='TBL'></Card>
		<Card suit='TBL'></Card>
		<Card suit='TBL'></Card>
		<Card suit='TBL'></Card>
	</div>
</main>

<!-- Style -->

<style>
	main {
		display: grid;
		grid-template-columns: 1fr 2fr 4fr;
		grid-template-rows: 1fr 3fr;
		grid-template-areas: 
			'stock waste foundation'
			'tableau tableau tableau';
		width: 80%;
		height: 100%;
		margin: 0 auto;
		border: solid purple 1px;
		background-color: olivedrab;
		padding: 1rem;

	}

	main > * {
		/* border: solid green 1px; */
	}

	#stock, #waste, #foundation, #tableau {
		display: flex;
		justify-content: space-around;
	}

	#stock {
		grid-area: stock;
	}

	#waste {
		grid-area: waste;
	}

	#foundation {
		grid-area: foundation;
	}

	#tableau {
		grid-area: tableau;
	}
</style>