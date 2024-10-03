<script>
	// You can include any additional script logic here if needed
	// You can include any additional script logic here if needed
</script>

<!-- Container for the banner -->
<div class="container">
  <div class="mask">
    <div class="mask-text">Etscalibur</div>
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
    -webkit-background-clip: text; /* Clip the background to the text */
    background-image: url('https://i.redd.it/eh5sgcfd8ii81.gif'); /* Use the same image as background */
    background-size: cover; /* Ensure it covers the text */
    background-position: center; /* Center the image */
  }
</style>
