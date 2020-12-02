<script>


  import { icons } from "./paths";

  export let value = false;
  export let style = undefined;
  export let classes = undefined;
  export let id = undefined;
  export let size = 24;
  export let whenTrue = "empty";
  export let whenFalse = "empty";

  $: icon = value ? icons[whenTrue] : icons[whenFalse];

</script>


<svg xmlns="http://www.w3.org/2000/svg" width="{size}" height="{size}" viewBox="0 0 24 24" {style} {id} class={classes}>{@html icon}</svg>
