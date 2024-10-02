<script>
  import { onMount, onDestroy } from 'svelte';

  export let title = "Etscalibur";
  export let links = ["Acceuil", "À propos", "Mission", "Compétitions", "Équipe"];

  // State to determine if the header should be visible
  let showHeader = false;

  // Function to handle scroll events
  const handleScroll = () => {
    // Show the header when scrolled past the banner (let's say 80% of banner height)
    showHeader = window.scrollY > window.innerHeight * 0.3;
  };

  // Use `onMount` to ensure window access is in the browser
  onMount(() => {
    // Attach the scroll event listener
    window.addEventListener('scroll', handleScroll);

    // Clean up on component unmount
    return () => {
      window.removeEventListener('scroll', handleScroll);
    };
  });
</script>

<style>
  header {
    position: fixed;
    top: 0;
    left: 0;
    right : 0;
    width: full;
    background: rgba(0, 0, 0, 0.7); /* Darker, semi-transparent background */
    backdrop-filter: blur(12px);
    z-index: 1000;
    padding : 1rem;
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
    display: flex;
    justify-content: space-between;
    align-items: center;
    transition: transform 0.3s ease-in-out; /* Smooth slide-in effect */
    
    
  }

    h1 {
    font-family: 'Cyberion';
    font-weight: normal;
    font-style: normal;

    font-size: 3rem;
    margin: 0.5rem;
    color: var(--primary-color); /* Bright color for the title */
  }

  /* Show the header when the `show` class is applied */
  .show {
   display : block;
  }

  header:hover {
    background: rgba(0, 0, 0, 0.8); /* Darker background on hover */
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
    color: var(--primary-color); /* Orange highlight on hover */
  }

  nav a::after {
    content: "";
    display: block;
    width: 0;
    height: 2px;
    background: var(--primary-color); /* Animated underline effect */
    transition: width 0.3s;
  }

  nav a:hover::after {
    width: 100%;
  }
</style>

<!-- Header -->
<header>
 <h1 class={showHeader ? 'show' : 'display: none'}>ETScalibur</h1>
  <nav>
    <ul>
      {#each links as link}
        <li><a href="#">{link}</a></li>
      {/each}
    </ul>
  </nav>
</header>
