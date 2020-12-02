<script lang="coffeescript">


  import icons from "./paths.js"

  export value = false
  export style = undefined
  export classes = undefined
  export size = 24
  export whenTrue = "empty"
  export whenFalse = "empty"

  `$: icon = value ? icons[whenTrue] : icons[whenFalse]`

</script>


<svg xmlns="http://www.w3.org/2000/svg" width="{size}" height="{size}" viewBox="0 0 24 24" {style} class={classes}>{@html icon}</svg>
