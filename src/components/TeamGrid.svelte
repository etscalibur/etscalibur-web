<script lang="ts">
  import TeamCard from './TeamCard.svelte';
  interface SocialLinks {
    github?: string;
    linkedin?: string;
  }

  interface Person {
    name: string;
    position: string;
    description: string;
    imageUrl: string;
    socialLinks?: SocialLinks;
  }

  export let members: Person[] = [];
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
    margin: 0 auto;
    padding: 2rem;
    display: grid;
    gap: 2rem;
    grid-template-columns: 1fr;
    max-width: 1440px;
  }

  @media (min-width: 640px) {
    .grid {
      grid-template-columns: repeat(2, 1fr);
      padding: 2rem;
    }
  }

  @media (min-width: 1024px) {
    .grid {
      grid-template-columns: repeat(3, 1fr);
      padding: 3rem 4rem;
    }
  }
</style>
