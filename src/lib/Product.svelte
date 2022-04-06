<script>
    export let name = 'No Name';
    export let blurb = 'No blurb has been provided';
    export let src = './img/pro.png';
    export let alt = "Image couldn't be retrieved";
</script>

<div class="container product">
    <img {src} {alt} />
    <h3>{name}</h3>
    <p>{blurb}</p>
    <button class="buy">Buy Now</button>
</div>

<style>
    
</style>