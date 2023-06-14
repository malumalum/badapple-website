<script>

  import SocialIcons from '@rodneylab/svelte-social-icons'

  import Mission from "/src/lib/content/Mission.svelte"
  import NavBar from "/src/lib/content/NavBar.svelte"

  import jalilHeadshot from '/src/lib/images/headshot_ja.png'
  import veljkoHeadshot from '/src/lib/images/headshot_vp.png'
  import urosHeadshot from '/src/lib/images/headshot_uk.png'
  import zhaoHeadshot from '/src/lib/images/headshot_zl.png'

  let socialIconWidth = 28;
  let socialIconHeight = 28;

  const social = [
      { network: "linkedin", ja: "https://www.linkedin.com/in/jalilafnan/", vp: "https://www.linkedin.com/in/veljko-popov-b9220916/", uk: "https://www.linkedin.com/in/ukalabic/", zl: "https://www.linkedin.com/in/zhaojian-li-5278a662/"},
      { network: "mailto", ja: "mailto:jalil.afnan@badapple.ai", vp: "mailto:veljko.popov@badapple.ai"},
    ];

</script>

  <NavBar />

  <h1>Welcome to Bad Apple</h1>

  <Mission />

  <h2>Our co-founders:</h2>

  <div class="people">
    <div>
      <img src={jalilHeadshot} class="headshot" alt="Jalil Afnan" />
      <br><strong>Jalil Afnan, MD, MRCS</strong>
      <div class="socials">
      {#each social as { network, ja }}
      <div class="icon">
        <a href={ja} target="_blank"><SocialIcons {network} width={socialIconWidth} height={socialIconHeight} /></a>
      </div>
      {/each}
      </div>
    </div>
    <div>
      <img src={veljkoHeadshot} class="headshot" alt="Veljko Popov" />
      <br><strong>Veljko Popov, MD, PhD</strong>
      <div class="socials">
      {#each social as { network, vp }}
      <div class="icon">
        <a href={vp} target="_blank"><SocialIcons {network} width={socialIconWidth} height={socialIconHeight} /></a>
      </div>
      {/each} 
      </div>
    </div>
  </div>
  <div class="people">
    <div>
      <img src={urosHeadshot} class="headshot" alt="Uros Kalabic" />
      <br><strong>Uroš Kalabić, PhD</strong>
      <div class="socials">
      {#each social as { network, uk }}
      <div class="icon">
        <a href={uk} target="_blank"><SocialIcons {network} width={socialIconWidth} height={socialIconHeight} /></a>
      </div>
      {/each} 
      </div>
    </div>
    <div>
      <img src={zhaoHeadshot} class="headshot" alt="Zhaojian Li" />
      <br><strong>Zhaojian Li, PhD</strong>
      <div class="socials">
      {#each social as { network, zl }}
      <div class="icon">
        <a href={zl} target="_blank"><SocialIcons {network} width={socialIconWidth} height={socialIconHeight} /></a>
      </div>
      {/each} 
      </div>
    </div>
  </div>


  <h6>&copy; 2023 Bad Apple Inc.</h6>


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
    padding-right: min(50px, 5%);
    padding-left: min(50px, 5%);
  }
  .people {
    display: flex;
    justify-content: space-evenly; 
  }
  .socials {
    display: flex;
    justify-content: center;
  }
  .headshot {
    height: 256px;
  }
  .logo {
    width: 426px;
    padding: 1.5em;
    /*will-change: filter;*/
    filter: drop-shadow(0 0 2em #646cffaa) drop-shadow(0 0 2em #646cffaa) drop-shadow(0 0 2em #646cffaa) drop-shadow(0 0 2em #646cffaa);
  }
  .logo:hover {
    filter: drop-shadow(0 0 2em #ff3e00aa) drop-shadow(0 0 2em #ff3e00aa) drop-shadow(0 0 2em #ff3e00aa) drop-shadow(0 0 2em #ff3e00aa);
  }
  @media screen and (max-width: 539px) {
    .logo {
      width: 79%;
    }
  }
</style>
