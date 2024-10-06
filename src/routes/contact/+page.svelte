<script>
  import Header from '../../components/sections/Header.svelte';
  import Footer from '../../components/sections/Footer.svelte';
  import Cta from '../../components/CTA.svelte';
</script>

<Header />
<div class="container">
  <h1>Contact</h1>
  <Cta />
</div>
<Footer />

<style>
  @font-face {
    font-family: 'Cyberion';
    src:
      url('../lib/assets/CyberionDemo.woff2') format('woff2'),
      url('../lib/assets/CyberionDemo.woff') format('woff');
    font-weight: normal;
    font-style: normal;
    font-display: swap;
  }
  :global(:root) {
    --primary-color: #e40032;
    --secondary-color: #f0f0f0;
    --bg-color: #fafafa;
    --text-primary: black;
    --text-highlight: #e40032;
    --button-p: #343434;
    --button-p-hover: #e40032;
    --button-p-text: white;
  }

  .container {
    padding: 20vh;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    background-color: var(--bg-color);
    color: var(--text-primary);
    text-align: center;
    position: relative; /* Needed for absolutely positioning the images */
    overflow: hidden;
  }
</style>
