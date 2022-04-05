<script>
    import Carousel from '$lib/Carousel.svelte';
    import VideoSection from "$lib/videoSection.svelte";
    import Products from "$lib/Products.svelte";
    import RibbonAds from "$lib/RibbonAds.svelte"
    
    import * as contentful from "contentful" ;
    const client = contentful.createClient({
        space: "3q892y4ckspg",
        accessToken: "w_ghIFLSyjNtCW4BdthHMn8WH21jXSC54suwYdXvxxQ",
        environment: "master"
    });

    let beers = [];
    let seltzers = [];

    client.getEntries({
      content_type: "product",
      "fields.brand.sys.id": "6qgNhvX2JOgZ80ZWyaq4zk",
      "fields.type" : "Beer"
    }).then(response => {
       beers = response.items;
     }).catch(error => {
        console.log("Error in Beers");
        console.log(error);
    }); 

    client.getEntries({
      content_type: "product",
      "fields.brand.sys.id": "6qgNhvX2JOgZ80ZWyaq4zk",
      "fields.type" : "Seltzer"
    }).then(response => {
       seltzers = response.items;
     }).catch(error => {
        console.log("Error in Seltzers");
      console.log(error);
    }); 
   
  
    let ribbonAds = [
        {
            "heading" : "Buy Stuff",
            "blurb" : "We'bve got you covered from the starting line to the cheers."
        },{
            "heading" : "Buy Stuff 2",
            "blurb" : "Another Ad? AAAAAAAhhhhhhh!"
        }
    ]


</script>

<Carousel />
<VideoSection />
<Products 
    sectionTitle="Beers"
    products={beers}
/>
<Products 
    sectionTitle="Seltzers"
    products={seltzers} 
/>  
<RibbonAds 
    ads={ribbonAds}
/> 
       