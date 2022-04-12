<script>
    import VideoAd from "./VideoAd.svelte"
    export let ads;
  </script>

<div class="space two commercials section">

    
  
    {#each ads as ad}

        <div class="ad video">
            
            <VideoAd 
                headline={ad.fields.headline}
                url={ad.fields.url}
                title={ad.fields.headline}
                text={ad.fields.text}
                image={ad.fields.image.fields.file.url}
            />
                
        </div>

    {/each}

    



</div>  

<style>

</style>