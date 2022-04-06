
<script>
    export let headline = "Buy Stuff";
    export let text = "We'bve got you covered from the starting line to the cheers.";
    export let buttonLabel = "This is a button"
    export let src = "./img/ribbon_ad_02.jpg";
    
    let alt = "This is a placeholder for an alt tag"
</script>

<div class="ribbonAd">
    <img {src} {alt} />
        <div class="ribbon">
            <h3>{headline}</h3>
            <p>{text}</p>
            <button>{buttonLabel}</button>
        </div>
</div>

<style>
    
</style>