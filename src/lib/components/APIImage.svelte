<script>
    import { onMount } from "svelte";
  
      export let heading;
      export let text;
      export let image;
      export let query;
  
      let setImageTextValues = (desc, alt_desc) => {
          if (desc !== null) {
              if (desc.length < alt_desc.length) {
                  return;
              }
              else {
                  heading = alt_desc;
                  text = desc;
              }
          }
          else {
              heading = query;
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