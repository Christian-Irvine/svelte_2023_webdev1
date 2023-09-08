<script>
    import { tries } from "$lib.index.js";
    import { random } from "$lib.index.js";

    let x = 0;
    let z = 0;

    function Method() {
        x = x + 1;
        console.log("Clicked " + x + " times")
        z = Math.floor(Math.random() * 1000);
    }

</script>
    
<h1>{ z }</h1>

<div>
    <button class="button" on:click={()=>Method()}>
	    Click Me!
    </button>
</div>