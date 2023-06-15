<script>
  import SocialIcons from '@rodneylab/svelte-social-icons'

  export let headshot;
  export let width;
  export let height;

  export let social;
  export let item;

  export let title;

  let innerWidth = 0;

  const fullWidth = 600;
  $: imgWidth = innerWidth * 0.4;

</script>

<svelte:window bind:innerWidth />


<div>
  {#if innerWidth > fullWidth} <br>
    <img src={headshot} width=100% alt={title[item]} />
  {:else}
    <img src={headshot} width={imgWidth} alt={title[item]} />
  {/if} 
  <br><strong>{title[item]}</strong>
  <div class="socials">
  {#each social as { network, item }}
  <div class="icon">
    <a href={item} target="_blank"><SocialIcons {network} width={width} height={height} /></a>
  </div>
  {/each} 
  </div>
</div>

<style>
  .headshot {
    height: 341px;
  }
  .socials {
    display: flex;
    justify-content: center;
  }
  @media screen and (max-width: 539px) {
    .headshot {
      width: 95%;
      height: 95%;
    }
  }
</style>