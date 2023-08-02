<script>
    import Nav from "$lib/Nav.svelte";
</script>

<style>
    header {
        background-color: rgb(246, 122, 246);
        height: 100px;
        margin-bottom: 40px;
    }

    h1 {
        text-align: left; 
        color: white;
        font-family: "Bahnschrift", Helvetica, sans-serif;
        font-size: 85px;
        margin: 0;
        margin-left: 10px;
    }

    .title{
        width: 50%;
        float: left;
    }

    .nav{
        width: 50%;
        float: right;
    }

</style>

<header>
    <div class="title"><h1>Patriarchy</h1></div>
    <div class="nav"><Nav/></div>
    
    
</header>