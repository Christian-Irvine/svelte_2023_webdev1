<script>
    import ArticleImage from "$lib/components/ArticleImage.svelte";
    import { onMount } from "svelte";

    let horses = [];

    onMount(() => {
        const BASE_URL = "https://api.unsplash.com";
        const ACCESS_KEY = "L7AbVF4hNZYjPi5SEV4yrdvuZHLY5PLNbThntYAdK5" //8
        fetch(`${BASE_URL}/search/photos?query=horses&client_id=${ACCESS_KEY}`)
        .then(res => res.json())
        .then(data => {
        horses = data.results
        })
    })
</script>

<div>
    <h1>Gallery</h1>
    <div class="page">
        <ArticleImage
            heading="image"
            text="image"
            image="craftymcfish1.jpg"
        />
    </div>
</div>