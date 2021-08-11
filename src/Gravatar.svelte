<script>
  import md5 from "blueimp-md5-es6/js/md5.js";
  export let email = undefined;
  export let alternateDefault = undefined;
  export let altText = "Gravatar";
  export let style = undefined;
  export let id = undefined;
  export let classes = undefined;
  let gravatarHash = "";
  $: gravatarHash = md5(email);
</script>

{#if email}
  <img src="https://www.gravatar.com/avatar/{gravatarHash || ""}" {style} {id} class={classes} alt={altText}/>
{:else}
  {if alternateDefault}
    <img src="https://www.gravatar.com/avatar/unknown" {style} {id} class={classes} alt={altText}/>
  {:else}
    <img src="https://www.gravatar.com/avatar/unknown" {style} {id} class={classes} alt={altText}/>
  {/if}
{/if}
