<svelte:head>
    <link href='static\fonts\CARDC___.TTF' rel='stylesheet'>
</svelte:head>

<script>

    export let rank = 4;
    export let suit = 'HRT';

</script>


<main>
    <div id='card'>
        <span class='top left rank'>{rank}</span>
        <span class='bot right rank'>{rank}</span>
        <span class='suit'>{suit}</span>
    </div>

</main>


<style>
    @font-face {
        font-family: 'Cardio';
        font-style: normal;
        font-weight: 400;
        src: url('static\fonts\CARDC___.TTF'), format('ttf');
    }

    #card {
        display: flex;
        position: relative;
        width: 8rem;
        aspect-ratio: 1/1.4;

        background-color: whitesmoke;
        border-radius: 1rem;
        font-family: 'Cardio';
        font-size: 2em;
        --label-padding: 0.25rem;
    }

    .rank {
        position: absolute;
    }

    .suit {
        position: relative;
        margin: auto;
    }

    .top {
        top: var(--label-padding);
    }

    .bot {
        bottom: var(--label-padding);
    }

    .left {
        left: var(--label-padding);
    }

    .right {
        right: var(--label-padding);
    }
</style>