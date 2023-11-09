<!-- The Nav component sits inside of the header, it holds all of the buttons and the 'ME' text -->

<script>
    import { onMount } from 'svelte';

    let hamburgerActive = false;

    // Toggles the the hamburgerActive bool
    let ToggleHamburger = () => {
        hamburgerActive = !hamburgerActive;
    }
</script>

<nav>
    <div class="icon-header">
        <!-- Calls the ToggleHamburger method when the hamburger button is clicked -->
        <button class="hamburger-menu"><a on:click={ToggleHamburger}><i class="fa-solid fa-bars"></i></a></button>
    </div>
    <!-- Displays the buttons to navigate the pages -->
    <div class={!hamburgerActive ? "nav-buttons nav-hide" : "nav-buttons" }>
        <a href="/craftymcfish"><button class="header-button">Crafty</button></a>
        <a href="/chrissyfresh"><button class="header-button">Chrissy</button></a>
        <a href="/games"><button class="header-button">Games</button></a>
        <a href="/gallery"><button class="header-button">Gallery</button></a>
    </div>
</nav>
