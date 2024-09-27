<script>
  export let title = "Etscalibur";
  export let links = ["Acceuil", "À propos", "Mission", "Compétitions", "Équipe"];
</script>

<style>
  header {
    position: sticky;
    top: 0;
    width: full;
    background: rgba(0,0 , 0, 0.7); /* Darker, semi-transparent background */
    backdrop-filter: blur(12px);
    z-index: 1000;
    padding: 1rem 2rem;
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
    display: flex;
    justify-content: space-between;
    align-items: center;
    transition: background 0.3s ease-in-out;
    margin-bottom : -100px;
  }

  header:hover {
    background: rgba(0, 0, 0, 0.8); /* Darker background on hover */
  }

  h1 {
    color: #ff4500;
    font-size: 1.5rem;
    font-family: 'Poppins', sans-serif; /* Modern, sleek font */
    text-transform: uppercase;
    letter-spacing: 2px;
  }

  nav ul {
    display: flex;
    font-family: 'Poppins', sans-serif; /* Modern, sleek font */
    list-style: none;
    gap: 1.5rem;
    margin: 0;
    padding: 0;
  }

  nav a {
    font-family: 'Poppins', sans-serif; /* Modern, sleek font */
    color: #fff;
    font-weight: bold;
    text-decoration: none;
    font-size: 1rem;
    transition: color 0.2s ease-in-out;
  }

  nav a:hover {
    color: #ff4500; /* Greenish highlight on hover */
  }

  nav a::after {
    content: "";
    display: block;
    width: 0;
    height: 2px;
    background: #ff4500; /* Animated underline effect */
    transition: width 0.3s;
  }

  nav a:hover::after {
    width: 100%;
  }
</style>

<header>
  <h1>{title}</h1>
  <nav>
    <ul>
      {#each links as link}
        <li><a href="#">{link}</a></li>
      {/each}
    </ul>
  </nav>
</header>
