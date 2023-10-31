<!-- The component for taking in a list of items and displaying them -->

<script>
    // Importing heading and list items variables
    export let heading;
    export let items;
</script>

<!-- The HTML where it displays the heading and items -->
<div>
    <h3>{ heading }</h3>
    <!-- Looping over each item and displaying it as a list item in an unordered list -->
    <ul>
        {#each items as item}
            <li>{ item }</li>
        {/each}
    </ul>
</div>