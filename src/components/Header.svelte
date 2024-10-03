<script>
  import { onMount } from 'svelte';
  
  export let links = ['Acceuil', 'À propos', 'Mission', 'Compétitions', 'Équipe'];

  // State to determine if the header should be visible
  let showHeader = false;

  // Function to handle scroll events
  const handleScroll = () => {
    // Show the header when scrolled past 30% of the window height
    showHeader = window.scrollY > window.innerHeight * 0.3;
  };
  
  // Use `onMount` to ensure window access is in the browser
  onMount(() => {
    window.addEventListener('scroll', handleScroll);
    return () => {
      window.removeEventListener('scroll', handleScroll);
    };
  });

  $: headerClass = showHeader ? 'header' : 'header-top';
</script>

<!-- Header -->

<header class="{headerClass}">
    <h1>ETScalibur</h1>

  <nav>
    <ul>
      {#each links as link}
        <li><a href="#">{link}</a></li>
      {/each}
    </ul>
  </nav>
</header>

<style>
  header {
    position: fixed;
    top: 0;
    left: 0;
    right: 0;

    z-index: 1000;
    padding: 1rem;
    display: flex;
    justify-content: space-between;
    align-items: center;
    backdrop-filter: blur(12px);
    transition: background 0.3s ease, padding 0.3s ease, box-shadow 0.3s ease; /* Smooth transitions */
  }

  .header-top {
    background: var(--primary-color);
    color: var(--text-primary);
    transition: background 0.3s ease, padding 0.3s ease, box-shadow 0.3s ease; /* Smooth transitions */
  }

  .header {
    background: rgba(0, 0, 0, 0.7); /* Semi-transparent dark background */
    color: #fff;
    box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1); /* Add a shadow when scrolling */
  }

  h1 {
    font-family: 'Cyberion';
    font-weight: normal;
    font-style: normal;
    font-size: 3rem;
    margin: 0.5rem;
    color: var(--primary-color); /* Bright color for the title */
  }


  nav ul {
    display: flex;
    font-family: 'Poppins', sans-serif;
    list-style: none;
    gap: 1.5rem;
    margin: 0;
    padding: 0;
  }

  nav a {
    font-family: 'Poppins', sans-serif;
    color: #fff;
    font-weight: bold;
    text-decoration: none;
    font-size: 1rem;
    transition: color 0.2s ease-in-out;
  }

  nav a:hover {
    color: var(--primary-color); 
  }

  .header-top nav a:hover {
    color: var(--text-primary); 
  }

  nav a::after {
    content: '';
    display: block;
    width: 0;
    height: 2px;
    background: var(--primary-color); 
    transition: width 0.3s;
  }

  .header-top nav a::after {
    background: var(--text-primary); 
  }

  nav a:hover::after {
    width: 100%;
  }
</style>
