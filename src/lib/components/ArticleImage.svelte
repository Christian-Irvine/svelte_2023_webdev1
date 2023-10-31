<!-- The component for having an image, a title, and a paragraph (for non API images) -->

<script>
    // Importing the heading, text, and image directory parts of the component
    export let heading;
    export let text;
    export let image;
</script>

<!-- The HTML that displays the part to the screen -->
<div class="image-grid">
    <!-- The image part -->
    <div class="article-image" style="background-image:url({ image })"></div>
    <!-- The paragraph and title part -->
    <div class="image-flex">
        <h3>{ heading }</h3>
        <p>{ text }</p>
    </div>
</div>
