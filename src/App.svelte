<script>
  import Navbar from "./Navbar.svelte";
  import Artists from "./best-of-19/Artists.svelte";
  import DecadeArtists from "./best-of-decade/DecadeArtists.svelte";

  //List of tab items with labels and values
  let tabItems = [
    { label: "best of '19", value: 1 },
    { label: "best of decade", value: 2 }
  ];

  //current active tab
  let currentTab;
</script>

<style>
  :global(#container) {
    font-family: "Nunito";
    background-color: #001327;
    color: #fff;
    margin: 0;
    padding: 0;
  }

  /* Footer */
  .name,
  .fa-github {
    color: #fff;
  }

  .fa-github {
    margin-left: 1rem;
  }

  footer {
    display: flex;
    justify-content: center;
  }
</style>

<div id="container">
  <Navbar bind:activeTabValue={currentTab} items={tabItems} />

  <code class="language-text" />

  {#if 1 === currentTab}
    <Artists />
  {/if}

  {#if 2 === currentTab}
    <DecadeArtists />
  {/if}

  <!-- Footer -->
  <footer>
    <p class="name">©2020 Simon Olsen</p>

    <a target="_blank" href="https://github.com/FroyoNom">
      <i class="fab fa-github" />
    </a>

  </footer>
</div>
