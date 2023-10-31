<!-- The Header component with the nav inside and butons to navigate -->

<script>
    // Importing nav component to go inside
    import Nav from "$lib/components/Nav.svelte";

    // importing what animation should play
    export let fadeClass;
</script>

<!-- Setting animation to either nothing, show the header, or hide the header -->
<header class={ fadeClass }>
    <!-- Top left icon button to bring you to home page -->
    <div class="title">
        <a href="/">
            <button>
                <h2>ME</h2>
            </button>
        </a>
    </div>
    <!-- Putting Nav component into header -->
    <Nav/>
</header>