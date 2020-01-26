<script>
  import { Navbar } from "sveltestrap";
  import { onMount } from "svelte";

  let isOpen = false;
  const toggle = () => (isOpen = !isOpen);

  export let items = [];
  export let activeTabValue = 0;

  onMount(() => {
    //set default tab value
    if (Array.isArray(items) && items.length && items[0].value) {
      activeTabValue = items[0].value;
    }
  });

  const handleClick = tabValue => () => (activeTabValue = tabValue);
</script>

<style>
  .grid-items {
    display: grid;
    grid-template-columns: 1fr 1fr;
    justify-items: center;
    padding-left: 0;
    list-style: none;
    margin-top: 2rem;
    margin-left: 0;
  }

  span {
    padding: 0.5rem 1rem;
    cursor: pointer;
  }

  li {
    font-size: 1.1rem;
  }

  li.active > span {
    border-bottom: 4px solid #00c284;
  }

  .combined {
    margin-top: 2rem;
  }
  .combined > h1,
  h2 {
    line-height: 32px;
  }
  .combined > h1 {
    margin-bottom: 0;
  }
  .combined > h2 {
    margin: 0;
    padding: 0;
    color: #00c284;
  }

  /* Responsive */
  @media only screen and (max-width: 650px) {
    .grid-items {
      justify-items: flex-start;
      grid-template-columns: 1fr 1fr;
    }

    .combined {
      position: relative;
      min-width: 100%;
      justify-content: center;
      align-content: center;
      text-align: center;
    }
  }

  @media only screen and (max-width: 375px) {
    .grid-items {
      justify-items: flex-end;
      grid-template-columns: 1fr 1fr;
    }
  }
</style>

<div class="container">
  <Navbar dark>
    <div class="combined">
      <h1>simon's</h1>
      <h2>music wrapped</h2>
    </div>
    <header class="grid-container">
      <ul class="grid-items">
        {#if Array.isArray(items)}
          {#each items as item}
            <li class={activeTabValue === item.value ? 'active' : ''}>
              <span on:click={handleClick(item.value)}>{item.label}</span>
            </li>
          {/each}
        {/if}
      </ul>
    </header>
  </Navbar>
</div>
