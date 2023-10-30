<script>
    import APIImage from "$lib/components/APIImage.svelte";
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

    let headingText = `Here are a collection of ${ query } that relate to me because I like ${ query }`;

</script>

<h1>Gallery</h1>
<div class="page gallery">
    
    <Article
        heading="Some images";
        text={ headingText };
    />
        
    {#each results as result}
        <!-- {() => setImageTextValues(results.description, results.alt_description)} -->
        <APIImage
            image={ result.urls.regular }
            heading={ result.description }
            text={ result.alt_description }
            query={ query }
        />
    {/each}
</div>