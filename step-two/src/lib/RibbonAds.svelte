<script>
    import RibbonAd from '$lib/RibbonAd.svelte';
   export let ads = [];
</script>


<div class="section ribbonAds space">

    {#each ads as ad}
                
      <RibbonAd 
          heading="{ad.heading}"
          blurb="{ad.blurb}"
          url="{ad.url}"
          buttonText="{ad.buttonText}"
      />

  {/each}

</div>


<style>

</style>