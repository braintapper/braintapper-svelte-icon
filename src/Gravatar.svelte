<script lang="coffeescript">
  export gravatarHash = undefined
  export altText = "Gravatar"
</script>

{#if gravatarHash}
<img src="https://www.gravatar.com/avatar/{gravatarHash || ""}" alt={altText}/>
{:else}
<img src="https://www.gravatar.com/avatar/unknown" alt={altText}/>
{/if}
