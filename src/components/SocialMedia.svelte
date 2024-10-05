<script>
  import Icon from '@iconify/svelte';
  import { links } from '../data/links';
</script>

<div class="social-section">
  <a href={links.github} target="_blank" class="social-link">
    <Icon icon="mdi:github" class="icon" />
  </a>

  <a href={links.linkedin} target="_blank" class="social-link">
    <Icon icon="mdi:linkedin" class="icon" />
  </a>

  <a href={links.instagram} target="_blank" class="social-link">
    <Icon icon="mdi:instagram" class="icon" />
  </a>

  <a href={links.facebook} target="_blank" class="social-link">
    <Icon icon="mdi:facebook" class="icon" />
  </a>

  <a href={links.email} target="_blank" class="social-link">
    <Icon icon="mdi:email" class="icon" />
  </a>

  <a href={links.discord} target="_blank" class="social-link">
    <Icon icon="mdi:discord" class="icon" />
  </a>
</div>

<style>
  .social-section {
    display: flex;
    justify-content: center;
    align-items: center;
    gap: 40px;
    padding: 20px;
  }

  .social-link {
    color: white;
    text-decoration: none;
    transition: transform 0.3s ease;
    scale: 2;
  }

  .social-link:hover {
    transform: scale(1.2);
  }
</style>
