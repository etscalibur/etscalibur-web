<script>
  import { onMount } from 'svelte';

  export let links = [
    { name: 'Accueil', href: '/' },
    { name: 'À propos', href: '/#À propos' },
    { name: 'Mission', href: '/#Mission' },
    { name: 'Équipe', href: '/#Équipe' },
    { name: 'Compétitions', href: '/#Compétitions' },
    { name: 'Contact', href: '/contact' }
  ];

  let showHeader = false;
  let mobileMenuOpen = false;

  const handleScroll = () => {
    showHeader = window.scrollY > window.innerHeight * 0.3;
  };

  onMount(() => {
    window.addEventListener('scroll', handleScroll);
    return () => {
      window.removeEventListener('scroll', handleScroll);
    };
  });

  $: headerClass = showHeader ? 'header' : 'header-top';
</script>

<!-- Header -->
<header class={headerClass}>
  <h1>ETScalibur</h1>

  <button class="mobile-toggle" on:click={() => (mobileMenuOpen = !mobileMenuOpen)}>
    ☰
  </button>

  <nav class:open={mobileMenuOpen}>
    <ul>
      {#each links as link}
        <li><a href={link.href} on:click={() => (mobileMenuOpen = false)}>{link.name}</a></li>
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
    transition: background 0.3s ease, padding 0.3s ease, box-shadow 0.3s ease;
  }

  .header-top {
    background: var(--primary-color);
    color: var(--text-primary);
  }

  .header {
    background: rgba(0, 0, 0, 0.7);
    color: #fff;
    box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
  }

  h1 {
    font-family: 'Cyberion';
    font-size: 2rem;
    margin: 0;
    color: var(--primary-color);
  }

  nav ul {
    display: flex;
    list-style: none;
    gap: 1.5rem;
    margin: 0;
    padding: 0;
  }

  nav a {
    color: #fff;
    font-weight: bold;
    text-decoration: none;
    font-size: 1rem;
    position: relative;
  }

  nav a:hover {
    color: var(--primary-color);
  }

  nav a::after {
    content: '';
    display: block;
    width: 0;
    height: 2px;
    background: var(--primary-color);
    transition: width 0.3s;
  }

  nav a:hover::after {
    width: 100%;
  }

  .header-top nav a:hover {
    color: var(--text-primary);
  }

  .header-top nav a::after {
    background: var(--text-primary);
  }

  .mobile-toggle {
    display: none;
    background: none;
    border: none;
    font-size: 2rem;
    color: #fff;
    cursor: pointer;
  }

  /* Responsive */
  @media (max-width: 768px) {
    nav {
      position: absolute;
      top: 100%;
      left: 0;
      right: 0;
      background: inherit;
      display: none;
      flex-direction: column;
      align-items: center;
      padding: 1rem 0;
    }

    nav.open {
      display: flex;
    }

    nav ul {
      flex-direction: column;
      gap: 1rem;
    }

    .mobile-toggle {
      display: block;
    }
  }
</style>
