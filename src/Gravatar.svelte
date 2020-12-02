<script>
  export let gravatarHash = undefined;
  export let altText = "Gravatar";
  export let style = undefined;
  export let id = undefined;
  export let classes = undefined;
</script>

{#if gravatarHash}
  <img src="https://www.gravatar.com/avatar/{gravatarHash || ""}" {style} {id} class={classes} alt={altText}/>
{:else}
  <img src="https://www.gravatar.com/avatar/unknown" {style} {id} class={classes} alt={altText}/>
{/if}
