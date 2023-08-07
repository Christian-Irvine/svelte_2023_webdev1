<style>
    :global(body) {
        margin: 0;
        background-color: rgb(216, 203, 212);
    }

    .main{
        background-color: rgb(216, 203, 212);
        padding-left: 12%;
        padding-right: 12%;
    }

    .imgLeft{
        text-align: left;
    }

    .imgRight{
        text-align: right;
    }

    .textLeft{
        float: left;
        text-align: right;
        margin-block-end: 0;
        max-width: 40%;
    }

    .textRight{
        float: right;
        text-align: left;
        max-width: 38%;
        margin: 0;
    }

    h2{
        color: black;
        font-family: "Bahnschrift", Helvetica, sans-serif;
        font-size: 45px;
        margin-bottom: 0;
        margin-left: 1%;
        margin-right: 1%;
    }

    img{
        width:55%;
        border: 6px;
        border-style: outset;
        border-color: rgb(246, 122, 246);
    }

    p{
        text-align: left; 
        color: black;
        font-family: "Bahnschrift", Helvetica, sans-serif;
        font-size: 25px;
    }
</style>

<script>
    import Header from "$lib/Header.svelte";
    import Footer from "$lib/Footer.svelte";

</script>

<Header />

<div class="main">

    <div class="imgLeft">
        <h2>Horses On The Move</h2>
        <img src="horses_gallop.webp" alt="horses running">
        <p class="textRight">These horses are beautiful, look how they gallop!</p>
    </div>

    <div class="imgRight">
        <h2>Horses On The Spot</h2>
        <img src="horse_eat_grass.webp" alt="Horses standing around">
        <p class="textLeft">See these horses as they graze the field in the name of horses!</p>
    </div>
    
    <div class="imgLeft">
        <h2>A Herd Of Horses</h2>
        <img src="horse_field.jpg" alt="Horses on a field">
        <p class="textRight">This massive herd of horses is spreading it through the world!</p>
    </div>

    <div class="imgRight">
        <h2>Horses On The Beach</h2>
        <img src="horse_ocean.jpg" alt="Horses by the sea">
        <p class="textLeft">These horses are trying to spread to the seas. It is a shame that nobody there wasnts to listen.</p>
    </div>


</div>

<Footer />