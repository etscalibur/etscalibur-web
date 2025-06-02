<script>
  // Placeholder for additional logic
</script>

<div class="container" id="Acceuil">
  <div class="mask">
    <div class="mask-text">ETScalibur</div>
  </div>
</div>

<style>
  .container {
    margin: 0;
    display: flex;
    justify-content: center;
    align-items: center;
    height: 40vh;
    background-color: var(--primary-color);
    padding-top: 10vh;
  }

  .mask {
    position: relative;
    width: 100%;
    height: 100%;
    display: flex;
    justify-content: center;
    align-items: center;
    background-size: cover;
    background-position: center;
    text-align: center;
  }

  .mask-text {
    position: absolute;
    font-family: 'Cyberion', sans-serif;
    font-size: clamp(3rem, 10vw, 9rem); /* Responsive font size */
    color: transparent;
    background-image: url('https://i.redd.it/eh5sgcfd8ii81.gif');
    background-size: cover;
    background-position: center;
    background-clip: text;
    -webkit-background-clip: text;
    -moz-background-clip: text;
    -webkit-text-fill-color: transparent; /* Safari/Chrome */
    -moz-text-fill-color: transparent; /* Firefox */
  }

  @media (max-width: 768px) {
    .container {
      height: 30vh;
      padding-top: 5vh;
    }

    .mask-text {
      font-size: clamp(2rem, 12vw, 5rem); /* Smaller on mobile */
    }
  }

  @media (max-width: 480px) {
    .mask-text {
      font-size: clamp(1.5rem, 14vw, 4rem);
    }
  }
</style>
