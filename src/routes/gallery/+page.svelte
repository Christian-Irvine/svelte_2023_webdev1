<script>
    // Imports the Components used on the page
    import APIImage from "$lib/components/APIImage.svelte";
    import Article from "$lib/components/Article.svelte";
    import ArticleParagraph from "$lib/components/Articleparagraph.svelte";

    import { onMount } from "svelte";

    let results = [];
    const query = `fish`;

    // Code to get the images from the unsplash.com api
    onMount(async () => {
        const BASE_URL = "https://api.unsplash.com";
        const ACCESS_KEY = "L7AbVF4hNZYjPi5SEV4yrdvuZHLY5PLNbThntYAdK58" //8
        let response = await fetch(`${BASE_URL}/search/photos?query=${query}&client_id=${ACCESS_KEY}`)
        let data = await response.json();
        console.log(data);
        results = data.results;
    });

    let headingText = `Here are a collection of ${ query } that relate to me because I like ${ query }`;

</script>

<!-- Title and white space -->
<div class="title-div">
    <h1>Gallery</h1>
</div>

<!-- The page class div to have the contents alternating colour and gallery class to have alternating sides of of image  -->
<div class="page gallery">
    
    <Article
        heading="Some images";
        text={ headingText };
    />
    <!-- Puts all of the images on the page from the API -->
    {#each results as result}
        <APIImage
            image={ result.urls.regular }
            heading={ result.description }
            text={ result.alt_description }
            query={ query }
        />
    {/each}

    <ArticleParagraph
        text="Images from unsplash.com"
    />
</div>