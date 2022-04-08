<script>
    export let sectionTitle = 'Products';
    import Product from "./Product.svelte";
    // import * as contentful from "contentful" 
    export let products = [];
</script>

<div class="space section">

    <h2>Our { sectionTitle } </h2>
    
    <div class="space container products">
      
            {#each products as product}
               
                <Product 
                    name="{product.fields.name}"
                    blurb="{product.fields.blurb}"
                    src="{product.fields.profileImage.fields.file.url}"
                    
                />
            
            {/each}


    </div>  
</div>



