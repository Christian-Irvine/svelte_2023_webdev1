<script>
    import Header from "$lib/components/Header.svelte";
    import Footer from "$lib/components/Footer.svelte";

    let yPos;
</script>

<svelte:head>
    <link rel="stylesheet" href="css/main.css" />
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.2/css/all.min.css" 
    integrity="sha512-z3gLpd7yknf1YoNbCzqRKc4qyor8gaKU1qmn+CShxbuBusANI9QpRohGBreCFkKxLhei6S9CQXFEbbKuqLg0DA==" 
    crossorigin="anonymous" referrerpolicy="no-referrer" />
</svelte:head>

{#if yPos <= 0}
    <Header 
        fadeClass="header-show"
    />
{:else}
    <Header 
    fadeClass="header-hide"
    />
{/if}




<div class="main">

<slot />

</div>

<Footer />

<svelte:window bind:scrollY={ yPos }/>