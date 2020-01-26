<style>
  .container {
    display: grid;
    grid-template-columns: 0.75fr 1.5fr 0.75fr;
    margin-top: 4rem;
    margin-bottom: 4rem;
  }

  .best-of {
    opacity: 40%;
    margin: 0;
    font-size: 2rem;
    font-weight: 700;
  }

  .summary {
    opacity: 80%;
    font-size: 1.2rem;
  }

  /* Responsive */
  @media only screen and (max-width: 964px) {
    .container {
      grid-template-columns: 0.6fr 2fr 0.4fr;
    }
  }

  @media only screen and (max-width: 749px) {
    .container {
      grid-template-columns: 0.2fr 2.6fr 0.2fr;
    }
  }
</style>

<div class="container">
  <div />
  <div class="both">
    <h3 class="best-of">Best of 2019</h3>
    <p class="summary">
      Spotify’s Wrapped told me that I listened to Spotify for ~61,000 minutes.
      That’s a few thousand less than 2018. I think as my job promoted me to a
      higher position I couldn’t listen to my podcasts. I discovered Iaye and
      enjoyed Post Malones new album Hollywood’s Bleeding.
    </p>
  </div>
  <div />
</div>
