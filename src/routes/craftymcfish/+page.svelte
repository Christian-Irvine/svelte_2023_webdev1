<script>
    import Article from "$lib/components/Article.svelte";
    import ArticleList from "$lib/components/ArticleList.svelte";
    import ArticleYoutube from "$lib/components/ArticleYoutube.svelte";
</script>

<h1>CraftyMCFish</h1>

<div class="page">
    
    <Article 
        heading="Origins" 
        text="The name CraftyMCFish originated on 2016. I wanted to change my username to 'MCFish' however,
        that name was already taken so I decided to take the 'Crafty' part of my old username and slap it on the front to form 'CraftyMCFish'.
        The channel was founded on the 7th Febuary 2017. At the beggining the videos consisted of animations made in Mine-Imator every week.
        These videos were rather short, only being around 30 seconds long. I would spend about 3 hours on each video sometimes a little longer sometimes a little shorter.
        Slowly over the few months of making them the quality began to improve. Though it wasn't long before I stopped."
    />

    <ArticleList 
        heading="Places The Name CraftyMCFish Is Used"
        items={[
            "Youtube",
            "Discord",
            "Steam",
            "X",
            "Epic Games",
            "Roblox",
            "Microsoft",
            "Minecraft Java Edition",
            "Reddit",
            "Tik Tok",
        ]}    
    />

    <ArticleYoutube 
        heading="My Youtube Trailer" 
        link="https://www.youtube.com/embed/ekBDeKwy86I"
    />

    <Article 
        heading="AncientCraft" 
        text="After the animations I moved onto making Minecraft Lets Plays on the server I was currently on called ''AncientCraft''.
        My fellow players had suggested the idea to me and lots of them I still know today."
    />
    
    <Article 
        heading="My Own Server" 
        text="At one point I started my own Minecraft Server called ''FishMC'' (yes I know how original) and it is still going to this day! Though I did pass it on to some of the players,
        but they have kept it alive this whole time."
    />

    <ArticleYoutube 
        heading="My Most Viewed Video" 
        link="https://www.youtube.com/embed/FeIo7c5bG4Q?si=LFXPcolscTZU8VqR"
    />

    <Article 
        heading="OmathaCraft" 
        text="Eventually AncientCrafts time came to an end, but a few people were invited to another server called OmathaCraft (me included). 
        The most notable thing I did on there was digging a big hole documented by the video titled ''i dug a hole'' above."
    />

    <Article 
        heading="100 Days Challenge" 
        text="In 2023 I made a return to the CraftyMCFish Youtube channel, 
        with the hit series the ''100 Days Challenge''. It is by far my most popular series yet,
        and the channel has had massive growth since the beggining of it."
    />

    <Article 
        heading="Fantastica" 
        text="Also in 2023 I started another series where I play on the Fantastica SMP, 
        known as ''Fantsatica SMP'' funnily enough. I was invited to this server from OmathaCraft so its a big chain of 3 now! 
        It isn't doing quite as well as the 100 Days as they are longer videos, and a lot less personal. However, I have dug another big hole! so thats pretty fun."
    />
</div>