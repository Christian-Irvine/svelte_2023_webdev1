<script>
    import { onMount } from 'svelte';

    

    onMount(() => {

    });

    let ToggleHamburger = () => {
        console.log("Toggled");
    }
</script>

<nav>
    <div class="nav-buttons nav-hide">
        <a href="/craftymcfish"><button class="headerbutton">Crafty</button></a>
        <a href="/chrissyfresh"><button class="headerbutton">Chrissy</button></a>
        <a href="/games"><button class="headerbutton">Games</button></a>
        <a href="/gallery"><button class="headerbutton">Gallery</button></a>
    </div>
    <div class="icon-header">
        <button class="hamburger-menu"><a on:click={ToggleHamburger}><i class="fa-solid fa-bars"></i></a></button>
    </div>
</nav>
