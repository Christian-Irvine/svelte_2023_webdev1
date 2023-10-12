<script>
    import ArticleImage from "$lib/components/ArticleImage.svelte";
    import Article from "$lib/components/Article.svelte";
    import { onMount } from "svelte";

    let results = [];
    const query = `fish`;

    onMount(async () => {
        const BASE_URL = "https://api.unsplash.com";
        const ACCESS_KEY = "L7AbVF4hNZYjPi5SEV4yrdvuZHLY5PLNbThntYAdK58" //8
        let response = await fetch(`${BASE_URL}/search/photos?query=${query}&client_id=${ACCESS_KEY}`)
        let data = await response.json();
        console.log(data);
        results = data.results;
    });

    let description;
    let title;

    let setImageTextValues = (desc, alt_desc) => {
        if (desc !== null){
            if (desc.length < alt_desc.length){
                title = desc;
                description = alt_desc;
            }
            else {
                title = alt_desc;
                description = alt_desc;
            }
        }
        else {
            title = query;
            description = alt_desc;
        }
    };

    //{setImageTextValues(result.description, result.alt_desc)} //This line should replace the bad html foreach
</script>

<h1>Gallery</h1>
<div class="page gallery">
    
    <Article
        heading="Some images"
        text="Here are a collection of images that relate to me for various reasons"
    />

    {#each results as result}
        {#if result.description !== null}
            {#if result.description.length < result.alt_description.length}
                { title = result.description }
                { description = result.alt_description }
            {:else if result.description.length > result.alt_description.length}
                { description = result.description }
                { title = result.alt_description } 
            {/if}
        {:else}
            { title = query }
            { description = result.alt_description }
        {/if}

        <ArticleImage
            image={ result.urls.regular }
            heading={ title }
            text={ description }
        />
    {/each}
</div>