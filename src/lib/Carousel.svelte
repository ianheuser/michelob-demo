<script>

    export let ads = [];
    import { onMount } from 'svelte';

    onMount(async () => {

        let carouselAds, current;
        
        function next(){
            carouselAds = document.querySelectorAll('.carousel .ad');
            current = document.querySelector('.current');
            let nextSibling = current.nextElementSibling;

            if(!nextSibling){
                nextSibling = carouselAds[0];
            } 
            
            current.classList.remove('current');
            nextSibling.classList.add('current');
            
        }

        
        function back(){
            carouselAds = document.querySelectorAll('.carousel .ad');
            current = document.querySelector('.current');
            let prevSibling = current.previousElementSibling;
            let totalAds = carouselAds.length;
            
            if(!prevSibling){
                prevSibling = carouselAds[totalAds - 1];
            } 
            
            current.classList.remove('current');
            prevSibling.classList.add('current');
            
        }

        let nextButton = document.querySelector('#next');
        nextButton.addEventListener('click', next );
        
        let backButton = document.querySelector('#back');
        backButton.addEventListener('click', back );

    });

   
</script>


<div class="carousel section">

    <div id="carouselAds">
        {#each ads as ad }

            <div class:current={ad.fields.current == true} class="ad">
            
                <img class="carouselImage" src="{ad.fields.image.fields.file.url}" alt="This is the banner" />
                <div class="content">
                    {#if ad.fields.headline && ad.fields.text }
                        <h1>{ad.fields.headline}</h1>
                        <p>{ad.fields.text}</p>
                        <button>{ad.fields.buttonLabel}</button>
                    {/if}
                </div>

            </div>
        {/each}
    </div>
    <div id="controller">
        <button id="back" class="controller back">BACK</button>
        <button id="next" class="controller next">NEXT</button>
    </div>
</div>

<style>
    
    .ad .content{
        width: 100%;
        text-align: center;
        color: white;
        position: relative;
        top: 20%;
    }

    .ad .content h1 {
        font-size: 64px;
        text-transform: uppercase;
        font-weight: bold;
        padding: 0px;
        margin: 0px;
    }

    .ad .content p {
        font-size: 32px;
        font-weight: lighter;
    }

    .carouselImage {
        position: absolute;
        top: 0px;
        left: 0px;
        width: 100%;
    }

    .carousel.section .ad {
        display: none;
    } 

    .carousel.section .ad.current {
        display: block;
    } 

    .carousel.section {
        max-height: 601px;
    height: 600px;
    position: relative;
    overflow: hidden;
        
    }

    #carouselAds {
        display: flex;
    }

    #carouselAds .content {
        padding: 70px 25px;
    box-sizing: border-box;
    }

    #controller {
        position: relative;
        padding: 50px;
    }

    .carousel.section div {
        display: block;
    }

</style>