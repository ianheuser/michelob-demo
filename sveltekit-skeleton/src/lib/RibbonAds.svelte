<script>
  import RibbonAd from "./RibbonAd.svelte"
  export let ads;

</script>


<div class="section ribbonAds space">
  {#each ads as ad}
    <RibbonAd 
      headline="{ad.fields.headline}"
      text="{ad.fields.text}"
      buttonLabel="{ad.fields.buttonLabel}"
      src="{ad.fields.image.fields.file.url}"
     
    />
  {/each}
</div>


<style>

</style>