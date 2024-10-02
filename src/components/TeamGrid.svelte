<script>
	import TeamCard from './TeamCard.svelte';
	export let members = [];
</script>

<div class="grid">
  {#each members as member}
    <TeamCard
      name={member.name}
      position={member.position}
      description={member.description}
      imageUrl={member.imageUrl}
      socialLinks={member.socialLinks}
    />
  {/each}
</div>

<style>
  .grid {
    padding-left: 10rem;
    padding-right: 10rem;
    display: grid;
    grid-template-columns: 1fr;
    gap: 16px;
  }

  @media (min-width: 640px) {
    .grid {
      grid-template-columns: repeat(2, 1fr);
    }
  }

  @media (min-width: 1024px) {
    .grid {
      grid-template-columns: repeat(3, 1fr);
    }
  }
</style>
