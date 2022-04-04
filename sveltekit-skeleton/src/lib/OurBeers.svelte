<script>
    export let sectionTitle = 'Our Beers';
    import Beer from "./Beer.svelte";
</script>


<div class="space section ourBeers">
    <h2>{ sectionTitle } </h2>
    <div class="space container beers">

        <Beer 
            name="Michelob Ultra" 
            blurb="This is a great blurb about Michelob" 
            src="./img/profile_bottle_pure_gold.png" 
            alt="A profile view image of Michelob Ultra" 
        />
        <Beer 
            name="Michelob Ultra Pure Gold" 
            blurb="USDA Certified Organic Beer" 
            src="./img/profile_bottle_pure_gold.png" 
            alt="A profile view image of Michelob Ultra Pure Gold" 
        />
        <Beer 
            name="Michelob Ultra Amber Max" 
            blurb="Taste the Impossible" 
            src="./img/profile_can_amber.jpg" 
            alt="A profile view image of Michelob Ultra Amber Max" 
        />
        <Beer 
            name="Michelob Ultra Infusions" 
            blurb="Beer meets exotic fruit" 
            src="./img/profile_can_infusions.png" 
            alt="A profile view image of Michelob Ultra Infusions Can" 
        />
    </div>  
</div>


