<script>
    export let name = 'No Name';
    export let blurb = 'No blurb has been provided';
    export let src = './img/pro.png';
   
</script>

<div class="container product">
    <img {src} alt="This is a good product" />
    <h3>{name}</h3>
    <p>{blurb}</p>
    <button class="buy">Buy Now</button>
</div>

<style>
    
</style>