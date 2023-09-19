<script>
    export let heading;
    export let link;
</script>

<div>
    <div>
        <h3>{ heading }</h3>
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
</div>