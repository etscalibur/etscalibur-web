<script>
  export let year = new Date().getFullYear();
  export let text = '© ETScalibur';
  import SocialMedia from '../../components/SocialMedia.svelte';
</script>

<footer>
  <p>{text} - <span>{year}</span></p>
  <section>
    <p>Contactez nous</p>
    <SocialMedia />
  </section>
</footer>

<style>
  footer {
    bottom: 0;
    width: full;
    background: rgba(0, 0, 0, 1); /* Match header background */
    backdrop-filter: blur(12px);
    z-index: 1000;
    padding: 1.5rem 2rem;
    box-shadow: 0 -4px 8px rgba(0, 0, 0, 0.2);
    text-align: center;
    transition: background 0.3s ease-in-out;
  }

  footer:hover {
    background: rgba(0, 0, 0, 1); /* Darken on hover */
  }

  p {
    margin: 0;
    color: #fff;
    font-size: 1rem;
    letter-spacing: 1px;
  }

  p span {
    color: #ff4500; /* Greenish highlight for dynamic year */
  }

  section {
    padding-top: 20px;
  }
</style>
