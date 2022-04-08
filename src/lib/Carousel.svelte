<script>
import { add_location } from "svelte/internal";


    export let ads = [];
    
</script>


<div class="carousel section">

    {#each ads as ad }
        {console.log(ad.fields.image.fields.file.url)}
        <div class="ad">
            <img src="{ad.fields.image.fields.file.url}" alt="This is the banner" />
            <div class="content">
                <h1>{ad.fields.headline}</h1>
                <p>{ad.fields.text}</p>
                <button>{ad.fields.buttonLabel}</button>
            </div>

        </div>
    {/each}

    <button class="controller back">BACK</button>
    <button class="controller next">NEXT</button>
</div>

<style>
    .content {

    }

</style>