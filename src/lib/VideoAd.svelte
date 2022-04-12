<script>

   export let headline;
   export let url;
   export let title;
   export let text;
   export let image;

</script>


<div class="ad video">

    <h3>{headline}</h3>
    <img src="{image}" class="videoCover cover" alt="This is the cover" />
    
    <div class="ad video">
        <iframe width="572" height="322" 
        src={url}
        title={title}
        frameborder="0" 
        allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" 
        allowfullscreen>  </iframe>
    </div>

    <p>{text}</p>

</div>


<style>

    .videoCover {
        display: none;
    }

</style>