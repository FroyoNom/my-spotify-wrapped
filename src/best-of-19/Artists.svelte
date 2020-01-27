<script>
  import Summary from "./Summary.svelte";
  import Songs from "./Songs.svelte";
  import Podcasts from "./Podcasts.svelte";

  export let artists = [
    {
      class: "post-malone",
      image: {
        src: "https://i.ibb.co/WyvRc52/download.jpg",
        alt: "Hollywood's Bleeding Cover"
      },
      name: "Post Malone"
    },
    {
      class: "laye",
      image: {
        src: "https://i.ibb.co/ykxWZjR/7645426.png",
        alt: "Lonesome Album Cover"
      },
      name: "laye"
    },
    {
      class: "haviah",
      image: {
        src: "https://i.ibb.co/LCQRJrH/haviah.jpg",
        alt: "13th Floor Album Cover"
      },
      name: "Haviah Mighty"
    },
    {
      class: "system-of",
      image: {
        src: "https://i.ibb.co/jkNbwNp/System-Of-A-Down-Hypnotize.jpg",
        alt: "Hypnotize Album Cover"
      },
      name: "System of a Down"
    }
  ];
</script>

<style>
  .container {
    margin-bottom: 8rem;
  }

  .heading {
    display: grid;
    justify-items: center;
    font-size: 2rem;
    background: #083358;
    max-width: 394px;
    border-radius: 5px;
    padding: 5px 0;
    margin: 2rem 0 2rem 1.8rem;
  }

  h2 {
    margin: 0;
    font-size: 3rem;
  }

  .names {
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    justify-items: center;
    justify-content: flex-end;
    align-items: center;
    margin-bottom: 8rem;
  }

  .post-malone,
  .laye,
  .haviah,
  .system-of {
    padding: 0;
    box-shadow: -10px 10px #00c284;
    border-radius: 5px;
  }

  .images {
    border-radius: 5px 5px 0 0;
  }

  .artists {
    color: #333;
    font-weight: 700;
    background: #fff;
    padding-top: 0.7rem;
    height: 50px;
    width: 180px;
    text-align: center;
    border-radius: 0 0 5px 5px;
    margin: 0;
  }

  /* Responsive */
  @media only screen and (max-width: 1080px) {
    .heading {
      margin: 2rem 0 2rem 9rem;
    }

    .names {
      grid-template-columns: repeat(2, 1fr);
      grid-template-rows: repeat(2, 1fr);
    }

    .post-malone,
    .laye,
    .haviah,
    .system-of {
      margin: 2rem;
    }
  }

  @media only screen and (max-width: 767px) {
    .heading {
      margin: 2rem 0 2rem 4rem;
    }

    .names {
      grid-template-columns: repeat(1, 1fr);
      grid-template-rows: repeat(4, 1fr);
    }
  }

  @media only screen and (max-width: 414px) {
    .heading {
      margin: 2rem 0 1rem 0;
    }
  }
</style>

<Summary />

<div class="container">
  <div class="heading">
    <h2>Top Artists</h2>
  </div>
  <div class="together">

    <div class="names">
      {#each artists as artist}
        <div class={artist.class}>
          <img class="images" src={artist.image.src} alt={artist.image.alt} />
          <p class="artists">{artist.name}</p>
        </div>
      {/each}
    </div>
  </div>

  <Songs />

  <Podcasts />
</div>
