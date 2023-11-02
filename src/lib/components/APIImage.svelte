<!-- The Component for handling fetch data from Unsplash API to display images and text-->

<script>
    import { onMount } from "svelte";
  
    // Importing variables to use for displaying
    export let heading;
    export let text;
    export let image;
    export let query;
  
    // Checking if if the image has both descriptions and if so what is longer to set it to the title and if not to set the title to the query
      let SetImageTextValues = (desc, alt_desc) => {
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
      
      // Calling the SetImageTextValues method on load
      onMount(() => {
          SetImageTextValues(heading, text);
      });
  </script>
  
  <!-- The actual image and text part that displays on the page in two divs so they can alternate-->
  <div class="image-grid">
      <!-- The image part -->
      <div class="gallery-image" style="background-image:url({ image })"></div>
      <!-- The title and paragraph part -->
      <div class="image-flex">
          <h3>{ heading }</h3>
          <p>{ text }</p>
      </div>
  </div>