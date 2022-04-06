<script>
    import Carousel from '$lib/Carousel.svelte';
    import VideoSection from "$lib/videoSection.svelte";
    import OurBeers from "$lib/OurBeers.svelte";
    import RibbonAds from "$lib/RibbonAds.svelte"

    let beers = [{
            "name":"Michelob Ultra",
            "blurb":"This blurb is coming from the beers object",
            "src":"./img/profile_bottle_pure_gold.png",
            "alt":"A profile view image of Michelob Ultra"
        },{ 
            "name":"Michelob Ultra Pure Gold",
            "blurb":"USDA Certified Organic Beer",
            "src":"./img/profile_bottle_pure_gold.png",
            "alt":"A profile view image of Michelob Ultra Pure Gold"
        },{ 
            "name":"Michelob Ultra Amber Max",
            "blurb":"Taste the Impossible",
            "src":"./img/profile_can_amber.jpg",
            "alt":"A profile view image of Michelob Ultra Amber Max"
        },{ 
            "name":"Michelob Ultra Infusions",
            "blurb":"Beer meets exotic fruit",
            "src":"./img/profile_can_infusions.png",
            "alt":"A profile view image of Michelob Ultra Infusions Can"
        }];

    let seltzers = [{ 
            "name":"Michelob Ultra Organic Seltzer",
            "blurb":"Its only worth it if you enjoy it",
            "src":"./img/profile_can_seltzer.png",
            "alt":"A profile view image of Michelob Ultra Seltzer Can"
        }];

        let ads = [{ 
            "heading":"Buy Gear",
            "blurb":"We've got you covered from the starting line to the cheers",
            "url":"./img/profile_can_seltzer.png",
            "buttonText":"Buy Now"
        },{ 
            "heading":"Buy Michelob ULTRA",
            "blurb":"Find a refreshing pack of your favorite ULTRA near you.",
            "url":"./img/profile_can_seltzer.png",
            "buttonText":"Buy Now"
        }];
</script>

<Carousel />
<VideoSection />
<OurBeers 
    sectionTitle="Beers"
    beers={beers} 
/>
<OurBeers 
    sectionTitle="Seltzers"
    beers={seltzers} 
/>  
<RibbonAds ads={ads} /> 
       