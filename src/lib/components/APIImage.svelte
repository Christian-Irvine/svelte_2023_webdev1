<script>
    import { onMount } from "svelte";
  
    export let heading;
    export let text;
    export let image;
    export let query;
  
      let setImageTextValues = (desc, alt_desc) => {
          if (desc !== null) {
              if (desc.length < alt_desc.length) {
                  heading = heading.charAt(0).toUpperCase() + heading.slice(1);
                  return;
              }
              else {
                  heading = alt_desc.charAt(0).toUpperCase() + alt_desc.slice(1);
                  text = desc;
              }
          }
          else {
              heading = query.charAt(0).toUpperCase() + query.toLowerCase().slice(1);
              text = alt_desc;
          }
      };
  
      onMount(() => {
          setImageTextValues(heading, text);
      });
  </script>
  
  <div class="image-grid">
      <div class="gallery-image" style="background-image:url({ image })"></div>
      <div class="image-flex">
          <h3>{ heading }</h3>
          <p>{ text }</p>
      </div>
  </div>