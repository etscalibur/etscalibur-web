<script>
  import Header from '../components/sections/Header.svelte';
  import Footer from '../components/sections/Footer.svelte';
  import Banner from '../components/sections/Banner.svelte';
  import Apropos from '../components/sections/Apropos.svelte';
  import Mission from '../components/sections/Mission.svelte';
  import Equipe from '../components/sections/Equipe.svelte';
  import Competitions from '../components/sections/Competitions.svelte';
</script>

<div>
  <Header />
  <Banner />
  <Apropos />
  <Mission />
  <Equipe />
  <Competitions />
  <Footer />
</div>

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
  * {
    font-family: 'Poppins', sans-serif;
  }
</style>
