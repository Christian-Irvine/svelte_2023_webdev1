<script>
    export let heading;
    export let text;
    export let image;
</script>

<div class="image-grid">
    <div class="article-image" style="background-image:url({ image })"></div>
    <div class="image-flex">
        <h3>{ heading }</h3>
        <p>{ text }</p>
    </div>
</div>
