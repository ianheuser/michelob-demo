<script>
    import Carousel from '$lib/Carousel.svelte';
    import VideoSection from "$lib/videoSection.svelte";
    import Products from '$lib/Products.svelte'
    import * as contentful from "contentful" ;
    import RibbonAds from "$lib/RibbonAds.svelte"
    import { onMount } from 'svelte';

    let ribbonAds = [];
    let seltzers = [];
    let beers = [];
    let carouselAds = [];

    onMount(async () => {
      const client = contentful.createClient({
          space: "3q892y4ckspg",
          accessToken: "w_ghIFLSyjNtCW4BdthHMn8WH21jXSC54suwYdXvxxQ",
          environment: "master"
      });

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
          console.log("Error in Seltzers",error);
      }); 
    
      
      client.getEntries({
        content_type: "basicAd",
        "fields.type": "ribbon"
      }).then(response => {
        ribbonAds = response.items;
      }).catch(error => {
          console.log("Error in Ribbon");
          console.log(error);
      }); 
    
      client.getEntries({
        content_type: "adCarousel"
      }).then(response => {
        carouselAds = response.items[0].fields.ads;
       /* for (const cAd in carouselAds ){
          console.dir(carouselAds[cAd]);
        }*/
      }).catch(error => {
          console.log("Error in Carousel");
          console.log(error);
      }); 
  });
  
</script>

<Carousel
  ads={carouselAds}
/>

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


    