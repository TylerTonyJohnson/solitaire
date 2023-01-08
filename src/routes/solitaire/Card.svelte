<!-- // Scripts -->
<script>
	export let rank = 0;
	export let suit = 'SUT';
</script>

<svelte:head>
	<link href="static\fonts\CARDC___.TTF" rel="stylesheet" />
</svelte:head>



<!-- // Structure -->

<div id="card">
	<span class="rank top">{rank}</span>
	<span class="suit">{suit}</span>
	<span class="rank bot">{rank}</span>
	<!-- <span class='icon'>{suit}</span> -->
</div>

<!-- //  Style -->
<style>
	@font-face {
		font-family: 'Cardio';
		font-style: normal;
		font-weight: 400;
		src: url('static\fonts\CARDC___.TTF'), format('ttf');
	}

	#card {
		display: grid;
		grid-template-columns: 1fr 2fr 1fr;
		grid-template-rows: 1fr 1fr;
		grid-template-areas:
			'rankTop suit blank'
			'blank suit rankBot';
		width: 6rem;
		aspect-ratio: 1/1.4;

		background-color: whitesmoke;
		border-radius: 10px;
		font-family: 'Cardio';
		font-size: 2em;
		--label-padding: 0.25rem;
	}

    .rank {
        border: solid blue 1px;
    }

	.rank.top {
		grid-area: rankTop;
	}

	.rank.bot {
		grid-area: rankBot;
	}

	.suit {
		border: solid red 1px;
		grid-area: suit;
	}

</style>
