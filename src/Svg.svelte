<script>

  import { icons } from "./paths.js"
  
  export let id = undefined;
  export let size = 24; // px
  export let icon = "empty"; // just an empty square, can be placeholder
  export let classes = undefined;
  export let style = undefined;
  export let fill = undefined;

</script>


<svg xmlns="http://www.w3.org/2000/svg" width="{size}" height="{size}" viewBox="0 0 24 24" {id} {style} class={classes}><path d={icons[icon]} {fill}/></svg>