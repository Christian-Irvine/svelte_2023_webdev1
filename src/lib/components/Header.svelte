<!-- The Header component with the nav inside and butons to navigate -->

<script>
    import Nav from "$lib/components/Nav.svelte";

    export let fadeClass;
</script>

<header class={ fadeClass }>
    <div class="title">
        <a href="/">
            <button>
                <h2>ME</h2>
            </button>
        </a>
    </div>
    <Nav/>
</header>