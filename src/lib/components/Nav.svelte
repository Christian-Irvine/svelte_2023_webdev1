<script>
    import { onMount } from 'svelte';

    let buttonDiv;
    let hamburgerActive = false;

    onMount(() => {
        buttonDiv = document.getElementsByClassName("nav-buttons")[0];
        console.log(buttonDiv);
    });

    let ToggleHamburger = () => {
        hamburgerActive = !hamburgerActive;
        if (hamburgerActive) {
            buttonDiv.classList.remove("nav-hide");
        }
        else {
            buttonDiv.classList.add("nav-hide");
        }
    }
</script>

<nav>
    <div class="icon-header">
        <button class="hamburger-menu"><a on:click={ToggleHamburger}><i class="fa-solid fa-bars"></i></a></button>
    </div>
    <div class="nav-buttons nav-hide">
        <a href="/craftymcfish"><button class="header-button">Crafty</button></a>
        <a href="/chrissyfresh"><button class="header-button">Chrissy</button></a>
        <a href="/games"><button class="header-button">Games</button></a>
        <a href="/gallery"><button class="header-button">Gallery</button></a>
    </div>
</nav>
