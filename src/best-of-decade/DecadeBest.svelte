<style>
  .container {
    margin-bottom: 8rem;
    margin-top: 8rem;
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
    grid-template-columns: repeat(2, 1fr);
    justify-items: center;
    justify-content: flex-end;
    align-items: center;
  }

  .super-driver,
  .anime-project {
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
    }

    .super-driver,
    .anime-project {
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
    <h2>Artist / Song of the Decade</h2>
  </div>

  <div class="together">
    <div class="names">

      <div class="anime-project">
        <img
          class="images"
          src="https://i.ibb.co/bdVKnt9/44f752b9d82dca1c8c10648699a5a419f5e1b23b.jpg"
          alt="Anime Project Cover" />
        <p class="artists">Anime Project</p>
      </div>

      <div class="super-driver">
        <img
          class="images"
          src="https://i.ibb.co/WWQRsds/1371186264-Booklet-01.jpg"
          alt="Super Driver Cover" />
        <p class="artists">
          Super Driver
          <span>Aya Hirano</span>
        </p>
      </div>

    </div>
  </div>
</div>
