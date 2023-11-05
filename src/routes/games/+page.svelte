<!-- The Games page about all of the games I have made in the Unity Engine over the past year and a bit -->

<script>
    // Importing components used for this page
    import Article from "$lib/components/Article.svelte";
    import ArticleImage from "$lib/components//ArticleImage.svelte";
    import ArticleList from "$lib/components/ArticleList.svelte";
</script>

<!-- Title and div to have white space and title at top of page -->
<div class="title-div">
    <h1>Games</h1>
</div>

<!-- The page class div to have the contents alternating colour -->
<div class="page">
    <Article 
        heading="Games I've Made"
        text="Though I have never finished a game ive worked on, a few of them have come quite far and slowly over time they have increased in quality.
        I started making games about 2 weeks before the Polytech Game Jam in 2022 before partaking in said Game Jam. 
        I thought it would be fun to try and learn as much as possible in a short time and see if we could make anything playable.
        From that I discovered making games is something I would love to do as a career and is something I hope to do."
    />
    
    <!-- Article List takes array of strings to display list items -->
    <ArticleList 
        heading="Games I've Tried Making"
        items={[
            "Hospital Hands",
            "2D Fish Shooter",
            "James May and The Eight Cheeses",
            "God Save The Queen",
            "2D Fish Shooter 2",
            "Burgotage!",
            "Untitled Town Game",
            "2D Fish Shooter 3"
        ]}    
    />

    <ArticleImage
        heading="Hospital Hands"
        text="Hospital Hands was the first game I had a hand in making and is the game my group made at the 2022 Polytech Game Jam.
        The game was about you controlling your hands which were disconnected from your body.
        In the abandoned hospital you had to go around and collect all the parts of your body and reconnect all your limbs.
        It only broke like 50% of the time and for a first game in 2 days thats not too bad."
        image="Games/HospitalHands.png"
    />

    <ArticleImage
        heading="2D Fish Shooter"
        text="2D Fish Shooter is a basic 2D game where your mouse controls a gun and you have to click (shoot) fish as they swim past. 
        If too many fish get past you die.
        As days go on they get faster and spawn more so eventually it gets too much.
        Sadly the game got too hard to maintain because the code was abominbal so I eventually gave up."
        image="Games/2DFishShooter1.png"
    />

    <ArticleImage
        heading="James May The Eight Cheeses"
        text="James May The Eight Cheeses is a game very similar to Slender The Eight Pages, except instead of slenderman its James May and instead of pages its cheese.
        The premise is you have to collect all 8 Cheeses to win but each one you pick up James May gets faster and teleported close to you so you must escape that area quickly.
        This was one of the first 3D projects I attempted and I didn't make great use of LOD's so it ran really really poorly on my pretty good PC so I stopped development on that too."
        image="Games/JamesMay.png"
    />

    <ArticleImage
        heading="God Save The Queen"
        text="God Save The Queen was a game I decided to make around the sad demise of The Queen (Rest In Peace).
        You had to get the queen from one side of the map to the other where the Union Jack was without her falling or touching spikes or whatnot by placing things with a limited budget.
        I didn't get very far because I didn't really enjoy making the game too much, and also the code was pretty hard to maintain."
        image="Games/GodSaveTheQueen.png"
    />

    <ArticleImage
        heading="2D Fish Shooter 2"
        text="2D Fish Shooter 2 is a lot like the first 2D Fish Shooter except I was slightly better at programming it when I started in 2023. 
        This version got a lot further with a boss, a shop system, cooler animations, better pixel art, even health on the fish, different guns e.t.c. 
        The issue is after developing it for 6 months I once again got a lot better at programming and realised how the system wasn't great to maintain so moved on again."
        image="Games/2DFishShooter2.png"
    />

    <ArticleImage
        heading="Burgotage!"
        text="Burgotage! was my second Game Jam entry in the 2023 Game Makers Toolkit Game Jam. The theme was revered roles.
        So I took the concept of Papas burgeria and made it so you are trying to sabotage the burger place. So your own rival one could get all the customers.
        Overall for 48 hours I think it was quite successful and the code was horrible but it did work and I had no plans on continuing it."
        image="Games/Burgotage!.png"
    />

    <ArticleImage
        heading="Untitled Town Game"
        text="I never named it but I started working on a town building simulator game where the twist was it was first person.
        The hope was that it would feel more grounded and that you were the mayor rather than some god placing buildings from the sky.
        I never really got far as the scale of the project was absolutely massive and I got burned out within a couple weeks with what felt like little progress."
        image="Games/TownGame.png"
    />

    <ArticleImage
        heading="2D Fish Shooter 3"
        text="2D Fish Shooter 3 is actually quite different from the other two. This time you have a player and have to navigate around caves and the ocean, 
        all still to shoot fish. Currently the only thing that exists is swimming and proceedurall terrain. But over the 2023 summer I intend on making a lot of progress on it.
        Hopefully there isn't a need for a 2D Fish Shooter 4, and maybe a 3D Fish shooter one day."
        image="Games/2DFishShooter1.png"
    />
</div>