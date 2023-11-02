<!-- The component for adding youtube videos -->

<script>
    // Importing the heading and link to video
    export let heading;
    export let link;
</script>

<!-- The HTML that displays the video -->
<div>
    <h3>{ heading }</h3>
    <!-- The youtube part setting the title and setting link to play the right video -->
    <iframe 
        class="youtube" 
        width="100%" 
        src={ link } 
        title= { heading } 
        frameborder="0" 
        allow="accelerometer; autoplay; clipboard-write; encrypted-media; picture-in-picture; web-share" 
        allowfullscreen
    />
</div>