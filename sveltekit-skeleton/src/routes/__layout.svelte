<script>
    import Navigation from '$lib/Navigation.svelte';
    import '../styles/global.css';
</script>


<div id="main">
    <!-- split the logo and navigation out into two separate components -->
    <Navigation />

    <slot>
                
    </slot> 

    <!-- create Footer.svelte -->
    <div class="footer">
        This is the footer
    </div>

</div>