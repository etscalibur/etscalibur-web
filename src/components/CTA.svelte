<script>
</script>

<div>
  <button class="cta" on:click={() => alert('Get ready to rumble!')}>Rejoins la bataille!</button>
  <img class="gear" src="./gear.svg" alt="Top-left gear" />
  <img class="gears" src="./gears.svg" alt="Bottom-right gears" />
</div>

<style>
  .cta {
    position: relative;
    background-color: var(--button-p);
    color: var(--button-p-text);
    padding: 0.8rem 2rem;
    border: none;
    border-radius: 5px;
    font-size: 1.2rem;
    cursor: pointer;
    transition: background-color 0.3s;
    position: relative; /* To make hover animations apply to these buttons */
    z-index: 2;
  }

  .cta:hover {
    background-color: var(--button-p-hover);
  }

  /* Position and hide the SVGs initially */
  .gear,
  .gears {
    position: relative;
    width: 80px; /* Adjust size as needed */
    height: auto;
    transition:
      transform 0.5s,
      opacity 0.5s; /* Smooth transition for animations */
    opacity: 0; /* Hide initially */
  }

  .gear {
    position: absolute;
    transform: translate(40, -5) rotate(0deg);
  }

  .gears {
    position: absolute;
    transform: translate(0, 0);
  }

  /* Show and animate SVGs on button hover */
  .cta:hover + .gear {
    opacity: 1;
    transform: translate(-60px, -4px) rotate(360deg);
  }
  .cta:hover + .gear + .gears {
    opacity: 1;
    transform: translate(60px, -30px); /* Make it visible and move into view */
  }
</style>
