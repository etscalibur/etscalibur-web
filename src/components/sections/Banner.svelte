<script>
  // You can include any additional script logic here if needed
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
    height: 30vh;
    background-color: var(--primary-color); /* Background color */
    padding-top: 20vh;
  }

  .mask {
    position: relative;
    width: 100%;
    height: 100%;
    display: flex;
    justify-content: center;
    align-items: center;
    text-align: center;
    background-size: cover; /* Ensure the image covers the container */
    background-position: center; /* Center the image */
  }

  .mask-text {
    position: absolute;
    font-family: 'Cyberion', sans-serif; /* Use the same font as the container */

    font-size: 9rem; /* Same size as defined */
    color: transparent; /* Make the text transparent for masking */
    /* Clip the background to the text */
    background-clip: text; /* Standard for modern browsers */
    -webkit-background-clip: text; /* For WebKit-based browsers like Chrome, Safari */
    -moz-background-clip: text; /* For older versions of Firefox */
    background-image: url('https://i.redd.it/eh5sgcfd8ii81.gif'); /* Use the same image as background */
    background-size: cover; /* Ensure it covers the text */
    background-position: center; /* Center the image */
  }
</style>
