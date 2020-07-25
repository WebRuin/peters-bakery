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
  .wrapper::before {
    display: block;
    position: relative;
    content: "";
    top: -2px;
    left: 50%;
    width: 120px;
    height: 3px;
    margin-left: -60px;
    background-color: var(--white);
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
