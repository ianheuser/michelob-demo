<script>

    export let ads = [];
    import { onMount } from 'svelte';

	let current = true;

	onMount(async () => {
		current = false;
	});
</script>


<div class="carousel section">

    {#each ads as ad }
        
        <div class="ad">
            <img src="{ad.fields.image.fields.file.url}" alt="This is the banner" />
            <div class="content">
                <h1>{ad.fields.headline}</h1>
                <p>{ad.fields.text}</p>
                <button>{ad.fields.buttonLabel}</button>
            </div>

        </div>
        {console.log(current)}
    {/each}

    <button class="controller back">BACK</button>
    <button class="controller next">NEXT</button>
</div>

<style>
    .content {

    }

</style>