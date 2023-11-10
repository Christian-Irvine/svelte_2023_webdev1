<script>
    // Importing the header and footer to be in the page
    import Header from "$lib/components/Header.svelte";
    import Footer from "$lib/components/Footer.svelte";

    // the y scroll value of the page (bound in the html)
    let yPos;
    // If its the page has just been loaded
    let firstLoad = true;
</script>

<svelte:head>
    <!-- Linking in the main CSS stylesheet -->
    <link rel="stylesheet" href="css/main.css" />
    <!-- Linking in the font-awesome icons stylesheet to use their icons on my pages -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.2/css/all.min.css" 
    integrity="sha512-z3gLpd7yknf1YoNbCzqRKc4qyor8gaKU1qmn+CShxbuBusANI9QpRohGBreCFkKxLhei6S9CQXFEbbKuqLg0DA==" 
    crossorigin="anonymous" referrerpolicy="no-referrer" />
</svelte:head>

<!-- Setting the animations for the header to slide in and slide out based on if its the first load and if it has scrolled -->
{#if yPos <= 0 && !firstLoad}
    <Header 
        fadeClass="header-show"
    />
{:else if !firstLoad}
    <Header 
        fadeClass="header-hide"
    />
{:else if yPos > 0 && firstLoad} 
    <Header 
        fadeClass="header-hide"
    />
    { firstLoad = false }
{:else}
    <Header 
        fadeClass=""
    />
{/if}

<!-- The back to top button -->
<a href="#main">
    <!-- Only show it if its not at the top of the page -->
    <div class="back-to-top { firstLoad ? "" : yPos > 0 ? "back-to-top-show" : "back-to-top-hide"}">
        <i class="fa-solid fa-angle-up"/>
    </div>
</a>

<!-- main div for all pages with id to link to it -->
<div class="main" id="main">

    <!-- The slot where the rest of the pages go into that use the layout file -->
<slot />

</div>

<!-- The footer component -->
<Footer />

<!-- Binding the yPos variable to be of the pixels scrolled value on the page -->
<svelte:window bind:scrollY={ yPos }/>