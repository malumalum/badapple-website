<script>

  import NavBar from "/src/lib/content/NavBar.svelte"

  import Logo from "/src/lib/images/logo.png"

  let innerWidth = 0;

  const fullWidth = 555;
  $: imgWidth = innerWidth * 0.9;

</script>

<svelte:window bind:innerWidth />

  <NavBar />

  <div style="margin: auto; height=100vh; text-align:center">
    <a href="/about">
      {#if innerWidth > fullWidth}
        <img src={Logo} alt="logo" width="500" />
      {:else}
        <img src={Logo} alt="logo" width={imgWidth} />
      {/if} 
    </a>

    <h6>&copy; 2023 Bad Apple Inc.</h6>
  </div>

<style>
  :global(body) {
    background-color: #ffffff;
    color: #000000;
    transition: background-color 0.3s;
    margin: 100px auto;
    text-align: center;
    display: grid;
    font-family: "Palatino", serif;
    max-width: 900px;
  }
</style>
