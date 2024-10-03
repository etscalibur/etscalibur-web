<script>
  import Header from '../components/Header.svelte';
  import Footer from '../components/Footer.svelte';
  import Banner from '../components/Banner.svelte';
  import Apropos from '../components/Apropos.svelte';
  import Mission from '../components/Mission.svelte';
  import Equipe from '../components/Equipe.svelte';
  import Competition from '../components/Competition.svelte';
</script>

<Header />
<Banner />
<Apropos />
<Mission />
<Equipe />
<Competition />
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
</style>
