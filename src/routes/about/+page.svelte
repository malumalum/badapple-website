<script>

  import SocialIcons from '@rodneylab/svelte-social-icons'

  import HeadTile from "/src/lib/content/HeadTile.svelte"
  import Mission from "/src/lib/content/Mission.svelte"
  import NavBar from "/src/lib/content/NavBar.svelte"

  import jalilHeadshot from '/src/lib/images/headshot_ja.png'
  import veljkoHeadshot from '/src/lib/images/headshot_vp.png'
  import urosHeadshot from '/src/lib/images/headshot_uk.png'
  import zhaoHeadshot from '/src/lib/images/headshot_zl.png'

  let socialIconWidth = 28;
  let socialIconHeight = 28;

  const title = { ja: "Jalil Afnan, MD, MRCS", vp: "Veljko Popov, MD, PhD", uk: "Uroš Kalabić, PhD", zl: "Zhaojian Li, PhD"};

  const social = [
      { network: "linkedin", ja: "https://www.linkedin.com/in/jalilafnan/", vp: "https://www.linkedin.com/in/veljko-popov-b9220916/", uk: "https://www.linkedin.com/in/ukalabic/", zl: "https://www.linkedin.com/in/zhaojian-li-5278a662/"},
      { network: "mailto", ja: "mailto:jalil.afnan@badapple.ai", vp: "mailto:veljko.popov@badapple.ai"},
    ];

</script>

  <NavBar />

  <h1>Welcome to Bad Apple</h1>

  <div class="justify">
    <Mission />
  </div>
  
  <h2>Our co-founders:</h2>

  <div class="people">
    <HeadTile headshot={jalilHeadshot} item={"ja"} width={socialIconWidth} height={socialIconHeight} social={social} title={title} />
    <HeadTile headshot={veljkoHeadshot} item={"vp"} width={socialIconWidth} height={socialIconHeight} social={social} title={title} />
  </div>
  <div class="people">
    <HeadTile headshot={urosHeadshot} item={"uk"} width={socialIconWidth} height={socialIconHeight} social={social} title={title} />
    <HeadTile headshot={zhaoHeadshot} item={"zl"} width={socialIconWidth} height={socialIconHeight} social={social} title={title} />
  </div>

  <h6>&copy; 2023 Bad Apple Inc.</h6>


<style>
  :global(body) {
    background-color: #ffffff;
    color: #000000;
    transition: background-color 0.3s;
    margin: 100px auto;
    display: grid;
    text-align: center;
    font-family: "Palatino", serif;
    max-width: 900px;
    padding-right: min(50px, 5%);
    padding-left: min(50px, 5%);
  }
  .justify {
    text-align: justify;
    text-justify: inter-word;
  }
  .people {
    display: flex;
    justify-content: space-evenly; 
  }
</style>
