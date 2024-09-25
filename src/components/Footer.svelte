<script>
  export let year = new Date().getFullYear();
  export let text = "© Etscalibur";
</script>

<style>
  footer {
    position: sticky;
    bottom: 0;
    width: 100%;
    background: rgba(0, 0, 0, 0.6); /* Match header background */
    backdrop-filter: blur(12px);
    z-index: 1000;
    padding: 1.5rem 2rem;
    box-shadow: 0 -4px 8px rgba(0, 0, 0, 0.2);
    text-align: center;
    transition: background 0.3s ease-in-out;
  }

  footer:hover {
    background: rgba(0, 0, 0, 0.8); /* Darken on hover */
  }

  p {
    margin: 0;
    color: #fff;
    font-size: 1rem;
    font-family: 'Poppins', sans-serif;
    letter-spacing: 1px;
  }

  p span {
    color: #1db954; /* Greenish highlight for dynamic year */
  }

  a {
    color: #fff;
    text-decoration: none;
    font-weight: bold;
    transition: color 0.2s ease-in-out;
  }

  a:hover {
    color: #1db954; /* Greenish highlight on hover */
  }
</style>

<footer>
  <p>{text} - <span>{year}</span></p>
</footer>
