<!-- The Chrissy Fresh page about my music and generalised usage of the name -->

<script>
    // Importing Components that I use on page
    import Article from "$lib/components//Article.svelte";
    import ArticleList from "$lib/components//ArticleList.svelte";
    import ArticleImage from "$lib/components//ArticleImage.svelte";
</script>

 <!-- Title and white space at top of page -->
<div class="title-div">
    <h1>Chrissy Fresh</h1>
</div>

<!-- The page class div to have the contents alternating colour -->
<div class="page">
    <Article 
        heading="Origins"
        text="Chrissy Fresh started as the name I posted music under. And eventually became a name I went by online, for more personal things. 
        For example my Instagram is called chrissy_fresh even though very little of what I post on there is about music. Its it just my online username for non gaming related things."
    />

    <ArticleList 
        heading="Classic Chrissy Fresh Songs" 
        items = {[
            "Luv or Somethin'", 
            "All I Want For Fortmas Is Vbucks",
            "Empty House With An Open Door"
        ]}
    />

    <ArticleImage
        heading="Luv or Somethin'" 
        text="Luv or Somethin' was my first song I released for Valentines Day in 2020 (even if it was a few days late). It was created within a week with me writing the lyrics,
        and a friend of mine playing the guitar. We went over to another friend to record it one day, but all of the things we got didn't line up so we had to record it on our phones and send it to friend 2.
        And that abomination of a song creation week is half the reason it is so bad. The other reason was I didn't sing I just talked."
        image="LuvOrSomethin.png"
    />

    <Article 
        heading="Luv or Somethin'" 
        text="Luv or Somethin' was my first song I released for Valentines Day in 2020 (even if it was a few days late). It was created within a week with me writing the lyrics,
        and a friend of mine playing the guitar. We went over to another friend to record it one day, but all of the things we got didn't line up so we had to record it on our phones and send it to friend 2.
        And that abomination of a song creation week is half the reason it is so bad. The other reason was I didn't sing I just talked."
    />

    <Article 
        heading="All I Want For Fortmas Is Vbucks" 
        text="My second song which I don't like to talk about is a Fortnite parody of the classic song ''All I Want For Christmas Is You'''. 
        I wrote it sometime in december one year and then never did much with it. Then in October I thought ''You know what'd be funny, if I made a Fortnite Christmas song in October''.
        So I did. I decided to play the ukulele as I wasn't very good at guitar at the time and it is what it is now."
    />

    <Article 
        heading="Empty House With An Open Door" 
        text="This song I wrote in 2022, when I was getting slightly better at guitaring. Its a very deep song about love and loss. And 100% fictional which makes it very funny.
        in 2023 I decided I wanted another Valentines Day Song, so I went back to friend 2s house and went ham. This time though we both were more experienced and we actually produced an absolute banger.
        We even got an old friend I hadn't spoken to in over a decade to play the bass guitar (which slaps by the way)."
    />
</div>
