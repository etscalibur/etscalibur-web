<script>
  import Header from '../components/Header.svelte';
  import Footer from '../components/Footer.svelte';
  import Banner from '../components/Banner.svelte';
  import Apropos from '../components/Apropos.svelte';
  import Mission from '../components/Mission.svelte';
  import Equipe from '../components/Equipe.svelte';
  import Competition from '../components/Competition.svelte';

</script>
<style>

  @font-face {
    font-family: 'Cyberion';
    src: url('../lib/assets/CyberionDemo.woff2') format('woff2'),
        url('../lib/assets/CyberionDemo.woff') format('woff');
    font-weight: normal;
    font-style: normal;
    font-display: swap;
}
  :global(:root){
  --primary-color:  #E40032;
  --bg-color: #FAFAFA;
  --text-primary: black;
  --text-highlight: #E40032;
  --button-p : #343434;
  --button-p-hover : #E40032;
  --button-p-text : white ;

  }

</style>

<Header />
<Banner />
<Apropos />
<Mission />
<Equipe />
<Competition />
<Footer />
<h1 style="font-family: 'Cyberion Demo'; font-weight: normal; font-style: normal;">Cyberion Demo</h1>
<h1>Hello </h1>
