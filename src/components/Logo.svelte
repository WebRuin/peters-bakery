<style>
  .logo {
    position: absolute;
    top: 50%;
    left: 50%;
    width: 300px;
    height: 300px;
    border-radius: 50%;
    color: var(--darkTeal);
    border: 2px solid var(--white);
    box-shadow: 0 0 0 5px var(--hotPink), 0 0 0 10px var(--teal),
      0 0 0 15px var(--white);
    margin-top: -150px;
    margin-left: -150px;
    align-items: center;
    background-color: var(--gold);
  }

  p {
    margin: 0;
    padding: 0;
    text-align: center;
  }

  .wrapper {
    position: relative;
    width: 65%;
    margin: 1.25rem auto 1rem auto;
  }

  .est,
  .description {
    margin: 0;
    font-weight: bold;
    font-size: 1.5rem;
    text-transform: uppercase;
  }

  .top {
    margin: -0.6rem 0 -1rem 0;
  }

  .bottom {
    margin: -2rem 0 -0.5rem 0;
  }

  .est {
    margin-top: 2rem;
    margin-bottom: -14px;
  }

  .name {
    position: relative;
    z-index: 2;
    font-size: 3.75rem;
    font-family: "Pacifico", cursive;
  }

  .description {
    font-size: 1rem;
    padding: 0;
  }
  @media (max-width: 1000px) {
    .logo {
      width: 150px;
      height: 150px;
      box-shadow: 0 0 0 3px var(--hotPink), 0 0 0 6px var(--teal),
        0 0 0 9px var(--white);
      margin-top: -75px;
      margin-left: -75px;
    }
    .wrapper {
      margin: 0.625rem auto 0.5rem auto;
    }
    .wrapper::after {
      display: block;
      position: relative;
      content: "";
      bottom: -2px;
      left: 50%;
      width: 120px;
      height: 3px;
      margin-left: -60px;
      background-color: var(--white);
    }
    .wrapper::before {
      width: 60px;
      height: 3px;
      margin-left: -30px;
    }
    .wrapper::after {
      width: 60px;
      height: 3px;
      margin-left: -30px;
    }

    .est,
    .description {
      font-size: 0.75rem;
    }

    .top {
      margin: -0.3rem 0 -0.5rem 0;
    }

    .bottom {
      margin: -1rem 0 -0.25rem 0;
    }

    .est {
      margin-top: 1rem;
      margin-bottom: -7px;
    }

    .name {
      z-index: 2;
      font-size: 1.875rem;
    }

    .description {
      font-size: 0.5rem;
    }
  }
</style>

<div class="logo">
  <p class="est">Est. 1936</p>
  <div class="wrapper">
    <p class="name top">Peter's</p>
    <p class="name bottom">Bakery</p>
  </div>
  <p class="description">Your neighborhood</p>
  <p class="description">baker</p>
</div>
