<script>
  export let songs = [
    {
      class: "super-driver",
      image: {
        src: "https://i.ibb.co/WWQRsds/1371186264-Booklet-01.jpg",
        alt: "Super Driver Cover"
      },
      name: "Super Driver",
      artists: "Aya Hirano"
    },
    {
      class: "polaroid",
      image: {
        src: "https://i.ibb.co/TTb9kKq/fd98c51048e2baede0a40b3c60e73f58.jpg",
        alt: "Polaroid Album Cover"
      },
      name: "Polaroid",
      artists: "Imagine Dragons"
    },
    {
      class: "beachan",
      image: {
        src: "https://i.ibb.co/r3Hc560/81-MLV40y-J8-L-SS500.jpg",
        alt: "Beachan-Robot Cover"
      },
      name: "Beachan-Robot",
      artists: "Lady-Baby"
    },
    {
      class: "kick-me",
      image: {
        src: "https://i.ibb.co/VpgBvC7/SWSKMSingle.png",
        alt: "Kick Me Cover"
      },
      name: "Kick Me",
      artists: "Sleeping with Sirens"
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
    max-width: 620px;
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

  .super-driver,
  .polaroid,
  .beachan,
  .kick-me {
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

  span {
    display: block;
    font-size: 0.7rem;
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

    .super-driver,
    .polaroid,
    .sicker,
    .women-colour {
      margin: 2rem;
    }
  }

  @media only screen and (max-width: 767px) {
    .heading {
      margin: 2rem 0 2rem 4rem;
      text-align: center;
    }

    .names {
      grid-template-columns: repeat(1, 1fr);
      grid-template-rows: repeat(4, 1fr);
    }
  }

  @media only screen and (max-width: 414px) {
    .heading {
      margin: 2rem 0 1rem 0;
      text-align: center;
    }
  }
</style>

<div class="container">
  <div class="heading">
    <h2>Songs of the Decade</h2>
  </div>
  <div class="together">
    <div class="names">

      {#each songs as song}
        <div class={song.class}>
          <img class="images" src={song.image.src} alt={song.image.alt} />
          <p class="artists">
            {song.name}
            <span>{song.artists}</span>
          </p>
        </div>
      {/each}

    </div>
  </div>
</div>
