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

  .sunflower,
  .summer-time,
  .sicker,
  .women-colour {
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

    .sunflower,
    .summer-time,
    .sicker,
    .women-colour {
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
    <h2>Top Songs</h2>
  </div>
  <div class="together">
    <div class="names">

      <div class="sunflower">
        <img
          class="images"
          src="https://i.ibb.co/30rMvzL/maxresdefault.jpg"
          alt="Sunflower Cover" />
        <p class="artists">
          Sunflower
          <span>Post Malone (feat. Swae Lee)</span>
        </p>
      </div>

      <div class="summer-time">
        <img
          class="images"
          src="https://i.ibb.co/DzT1bgN/91b9b-N06-JQL-SS500.jpg"
          alt="Summer Time Cover" />
        <p class="artists">
          Summer Time
          <span>Tish Hyman (feat. Kill Nigel)</span>
        </p>

      </div>

      <div class="sicker">
        <img
          class="images"
          src="https://i.ibb.co/2qgFmq3/maxresdefault-1.jpg"
          alt="Sicker Cover" />
        <p class="artists">
          Sicker
          <span>laye</span>
        </p>

      </div>

      <div class="women-colour">
        <img
          class="images"
          src="https://i.ibb.co/Y3XsXnx/haviah-mighty-1200w-2.jpg"
          alt="13th Floor album cover" />
        <p class="artists">
          In Women Colour
          <span>Haviah Mighty</span>
        </p>

      </div>
    </div>
  </div>
</div>
