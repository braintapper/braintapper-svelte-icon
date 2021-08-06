<script>

  export let value = undefined;
  export let color = "light-gray";
  export let size = 24;

  export let style = undefined;
  export let id = undefined;
  export let classes = undefined;

  let fillColor, path;

  fillColor = function(val) {
    switch (val) {
      case "light-gray":
        return "var(--lightest-gray)";
      case "gray":
        return "var(--gray)";
      case "dark-gray":
        return "var(--darker-gray)";
      case "green":
        return "var(--green)";
      case "yellow":
        return "var(--yellow)";
      case "orange":
        return "var(--orange)";        
      case "red":
        return "var(--red)";
      case "blue":
        return "var(--blue)";
    }
  };

  // these are hard coded to 0, 25, 50, 75 and 100%

  path = function(val) {
    switch (val) {
      case 0:
        return "M12,20A8,8 0 0,1 4,12A8,8 0 0,1 12,4A8,8 0 0,1 20,12A8,8 0 0,1 12,20M12,2A10,10 0 0,0 2,12A10,10 0 0,0 12,22A10,10 0 0,0 22,12A10,10 0 0,0 12,2Z";
      case 25:
        return "M12 2C17.5 2 22 6.5 22 12C22 17.5 17.5 22 12 22C6.5 22 2 17.5 2 12C2 6.5 6.5 2 12 2M12 4C7.58 4 4 7.58 4 12C4 16.42 7.58 20 12 20C16.42 20 20 16.42 20 12C20 7.58 16.42 4 12 4M12 5C15.87 5 19 8.13 19 12H12V5Z";
      case 50:
        return "M12 2C17.5 2 22 6.5 22 12C22 17.5 17.5 22 12 22C6.5 22 2 17.5 2 12C2 6.5 6.5 2 12 2M12 4C7.58 4 4 7.58 4 12C4 16.42 7.58 20 12 20C16.42 20 20 16.42 20 12C20 7.58 16.42 4 12 4M12 5C15.87 5 19 8.13 19 12C19 15.87 15.87 19 12 19V5Z";
      case 75:
        return "M12 2C17.5 2 22 6.5 22 12C22 17.5 17.5 22 12 22C6.5 22 2 17.5 2 12C2 6.5 6.5 2 12 2M12 4C7.58 4 4 7.58 4 12C4 16.42 7.58 20 12 20C16.42 20 20 16.42 20 12C20 7.58 16.42 4 12 4M12 5C15.87 5 19 8.13 19 12C19 15.87 15.87 19 12 19C8.13 19 5 15.87 5 12H12V5Z";
      default:
        return "M12 5C15.87 5 19 8.13 19 12C19 15.87 15.87 19 12 19C8.13 19 5 15.87 5 12C5 8.13 8.13 5 12 5M12 2C17.5 2 22 6.5 22 12C22 17.5 17.5 22 12 22C6.5 22 2 17.5 2 12C2 6.5 6.5 2 12 2M12 4C7.58 4 4 7.58 4 12C4 16.42 7.58 20 12 20C16.42 20 20 16.42 20 12C20 7.58 16.42 4 12 4Z";
    }
  };


  $: d = path(value || 0);
  $: fill = fillColor(color);
</script>

<svg xmlns="http://www.w3.org/2000/svg" width="{size}" height="{size}" version="1.1" viewBox="0 0 24 24" {style} {id} class={classes}>
  <path {fill} {d}/>
</svg>
