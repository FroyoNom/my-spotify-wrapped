<script>
  import DecadeSongs from "./DecadeSongs.svelte";
  import DecadeBest from "./DecadeBest.svelte";
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
    margin-bottom: 8rem;
  }

  .anime-project,
  .system-of,
  .kendrick,
  .post-malone {
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

    .anime-project,
    .system-of,
    .kendrick,
    .post-malone {
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

<DecadeBest />

<div class="container">
  <div class="heading">
    <h2>Artists of the Decade</h2>
  </div>
  <div class="together">
    <div class="names">
      <div class="anime-project">
        <img
          class="images"
          src="https://i.ibb.co/bdVKnt9/44f752b9d82dca1c8c10648699a5a419f5e1b23b.jpg"
          alt="" />
        <p class="artists">Anime Project</p>
      </div>
      <div class="system-of">
        <img
          class="images"
          src="https://i.ibb.co/jkNbwNp/System-Of-A-Down-Hypnotize.jpg"
          alt="Hyptonize album cover" />
        <p class="artists">System of A Down</p>
      </div>
      <div class="kendrick">
        <img
          class="images"
          src="https://i.ibb.co/ykxQN9L/220px-Kendrick-Lamar-Damn.png"
          alt="" />
        <p class="artists">Kendrick Lamar</p>
      </div>
      <div class="post-malone">
        <img
          class="images"
          src="https://i.ibb.co/WyvRc52/download.jpg"
          alt="Hollywoods Bleeding album cover" />
        <p class="artists">Post Malone</p>
      </div>
    </div>
  </div>

  <DecadeSongs />

</div>
