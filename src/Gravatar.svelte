<script>
  import * as md5 from "md5";
  export let email = undefined;
  export let altText = "Gravatar";
  export let style = undefined;
  export let id = undefined;
  export let classes = undefined;
  $: gravatarHash = md5(email);
</script>

{#if email}
  <img src="https://www.gravatar.com/avatar/{gravatarHash || ""}" {style} {id} class={classes} alt={altText}/>
{:else}
  <img src="https://www.gravatar.com/avatar/unknown" {style} {id} class={classes} alt={altText}/>
{/if}
