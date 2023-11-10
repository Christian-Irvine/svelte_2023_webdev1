<script>
    // Importing article component to use in the page
    import Article from "$lib/components/Article.svelte";
</script>

<!-- The big header text and div around it -->
<div class="title-div">
    <h1>Welcome!</h1>
</div>

<div class="page">
    <!-- A short welcoming description of who I am and what the page is about -->
    <Article
        heading="Hello There";
        text="I am Christian and this website is all about me and my various usernames on the internet. From Chrissy Fresh and my music to CraftyMCFish and my minecraft youtube videos."
    />

    <!-- A brief description of what CraftyMCFish is -->
    <Article
        heading="CraftyMCFish";
        text="CraftyMCFish is my gaming username on the internet.
        It is what I play games under but it is also the name my Youtube Channel goes by.
        On the channel I post Minecraft Gaming videos but plan to expand to other games in the future."
    />
    
    <!-- A Brief description of what Chrissy Fresh is -->
    <Article
        heading="Chrissy Fresh";
        text="Chrissy Fresh is my music and personal username on the internet.
        Primarily the name was for releasing music under, but I also ended up using the name for my accounts with more personal things on them.
        For example my instagram which has pictures of me and what i'm doing."
    />

    <!-- A Brief description of the games I have made -->
    <Article
    heading="Games I've Made";
    text="I have made a few games over the last year and a half mostly inside of the Unity Engine. 
    The games consist of silly horror game about James May to serious games about shooting 2D Fish with guns."
/>
</div>


