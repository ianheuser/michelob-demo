<script>
    export let sectionTitle = 'Beers';
    import Beer from "./Beer.svelte";
     
    export let beers;

</script>

<div class="space section ourBeers">

    <h2>Our { sectionTitle } </h2>
    
    <div class="space container beers">
      
            {#each beers as beer}
               
                <Beer 
                    name="{beer.name}"
                    blurb="{beer.blurb}"
                    src="{beer.src}"
                    alt="{beer.alt}"
                />
            
            {/each}


    </div>  
</div>


