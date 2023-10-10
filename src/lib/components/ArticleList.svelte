<script>
    export let heading;
    export let items;
</script>

<div>
    <h3>{ heading }</h3>
    <ul>
        {#each items as item}
            <li>{ item }</li>
        {/each}
    </ul>
</div>