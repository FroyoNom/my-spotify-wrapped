<script>
  export let podcasts = [
    {
      class: "tlpotl",
      image: {
        src: "https://i.ibb.co/MN9Rdbs/Last-Pod-logo.jpg",
        alt: "Last Pod Cover"
      },
      name: "Last Podcast on the Left"
    },
    {
      class: "serial-killers",
      image: {
        src:
          "https://i.ibb.co/h1bTyXL/uploads-2-F1577907239282-z6z3288q1u-c17561d515fd89c85bda757d149bf1ee-2-Fserialkillers-logo-noeyes.jpg",
        alt: "Serial Killers Cover"
      },
      name: "Serial Killers"
    },
    {
      class: "indie",
      image: {
        src:
          "https://i.ibb.co/0JfDH2w/d6332992cd3d807203c0c9c4a6734718899bc7b7.jpg",
        alt: "IndieHackers Cover"
      },
      name: "The IndieHackers Podcast"
    },
    {
      class: "no-sleep",
      image: {
        src: "https://i.ibb.co/87W9gWY/No-Sleep-Podcast-S4-Logo-1400.jpg",
        alt: "The NoSleep Podcast Cover"
      },
      name: "The NoSleep Podcast"
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
  }

  .tlpotl,
  .serial-killers,
  .indie,
  .no-sleep {
    padding: 0;
    box-shadow: -10px 10px #00c284;
    border-radius: 5px;
  }

  .images {
    border-radius: 5px 5px 0 0;
  }

  .podcasts {
    color: #333;
    font-weight: 700;
    background: #fff;
    padding-top: 0.7rem;
    height: 50px;
    width: 180px;
    text-align: center;
    border-radius: 0 0 5px 5px;
    margin: 0;
    font-size: 0.9rem;
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

    .tlpotl,
    .serial-killers,
    .indie,
    .no-sleep {
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

<div class="container">
  <div class="heading">
    <h2>Top Podcasts</h2>
  </div>
  <div class="together">
    <div class="names">
      {#each podcasts as podcast}
        <div class={podcast.class}>
          <img class="images" src={podcast.image.src} alt={podcast.image.alt} />
          <p class="podcasts">{podcast.name}</p>
        </div>
      {/each}
    </div>
  </div>
</div>
