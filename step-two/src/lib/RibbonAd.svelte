<script>
    export let heading = 'No Name';
    export let blurb = 'No blurb has been provided';
    export let url = './img/pro.png';
    export let buttonText = "Image couldn't be retrieved";
</script>


    <div class="ribbonAd">
        <img src={url} alt="Ad text" />
        <div class="ribbon">
            <h3>{heading}</h3>
            <p>{blurb}</p>
            <button class="buy">{buttonText}</button>
        </div>
    </div>

<style>
    
</style>