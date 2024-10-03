<script>
	export let name;
	export let position;
	export let description;
	export let imageUrl;
	export let socialLinks;
	import Icon from '@iconify/svelte';
	export let name;
	export let position;
	export let description;
	export let imageUrl;
	export let socialLinks;
	import Icon from '@iconify/svelte';
</script>

<div class="card">
  <img src={imageUrl} alt={name} class="image" />
  <div class="details">
    <div>
      <h3 class="name">{name}</h3>
      <p class="position">{position}</p>
      <p class="description">{description}</p>
    </div>
    <div class="social-links">
      {#if socialLinks.github}
        <a href={socialLinks.github} target="_blank">
          <Icon icon="mdi:github" width="24">
            <a href={socialLinks.github} target="_blank"> </a></Icon
          >
        </a>
      {/if}
      {#if socialLinks.linkedin}
        <a href={socialLinks.linkedin} target="_blank">
          <Icon icon="mdi:linkedin" width="24" />
        </a>
      {/if}
    </div>
  </div>
</div>

<style>
  .card {
    background-color: var(--secondary-color);
    color: var(--text-primary);
    border-radius: 8px;
    box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
    display: flex;
    padding: 16px;
  }

	.image {
		width: 128px;
		height: 128px;
		border-radius: 8px;
		object-fit: cover;
		margin-right: 16px;
	}
	.image {
		width: 128px;
		height: 128px;
		border-radius: 8px;
		object-fit: cover;
		margin-right: 16px;
	}

	.details {
		display: flex;
		flex-direction: column;
		justify-content: space-between;
	}
	.details {
		display: flex;
		flex-direction: column;
		justify-content: space-between;
	}

	.name {
		font-size: 1.25rem;
		font-weight: bold;
	}
	.name {
		font-size: 1.25rem;
		font-weight: bold;
	}

  .position {
    font-size: 0.875rem;
    color: var(--text-primary);
  }

	.description {
		margin-top: 8px;
	}
	.description {
		margin-top: 8px;
	}

  .social-links a {
    margin-right: 8px;
    color: inherit;
    text-decoration: none;
  }
</style>
