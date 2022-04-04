<script>
  import RibbonAd from "./RibbonAd.svelte"
  export let ads;

</script>


<div class="section ribbonAds space">
  {#each ads as ad}
    <RibbonAd 
      heading="{ad.heading}"
      blurb="{ad.blurb}"
    />
  {/each}
</div>


<style>

</style>