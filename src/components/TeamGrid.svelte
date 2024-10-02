<script>
  import TeamCard from './TeamCard.svelte';

  let teamMembers = [
    {
      name: 'Félix Lachance',
      position: 'Président',
      description: '',
      imageUrl: '',
      socialLinks: {
        github: 'https://github.com/',
        linkedin: 'https://www.linkedin.com/in/',
      },
    },
    {
      name: 'Zhi Sheng Trieu',
      position: 'VP tresorerie & Communication',
      description: '',
      imageUrl: 'https://zhisheng.me/wp-content/uploads/2023/04/Photo_Profil.jpg',
      socialLinks: {
        github: 'https://github.com/zhishengtrieu',
        linkedin: 'https://www.linkedin.com/in/zhishengtrieu/',
      },
    },
    {
      name: 'Alexandre Baudouin Vegas',
      position: 'VP tresorerie & Chef logiciel',
      description: '',
      imageUrl: '',
      socialLinks: {
        github: 'https://github.com/',
        linkedin: 'https://www.linkedin.com/in/',
      },
    },
    {
      name: 'Julien Giguère',
      position: 'Secrétaire',
      description: '',
      imageUrl: '',
      socialLinks: {
        github: 'https://github.com/',
      },
    },
    {
      name: 'Juan hihi',
      position: 'Chef innovation',
      description: '',
      imageUrl: '',
      socialLinks: {
        github: '  ',
        linkedin: 'https://www.linkedin.com/in/',
      },
    },
    {
      name: 'Victor Feliciello',
      position: 'VP compétitions & Chef mécanique',
      description: '',
      imageUrl: '',
      socialLinks: {
        github: '  ',
        linkedin: 'https://www.linkedin.com/in/',
      },
    },
    {
      name: 'Charles-Antoine Cusson',
      position: 'Chef électrique',
      description: '',
      imageUrl: '',
      socialLinks: {
        github: '  ',
        linkedin: 'https://www.linkedin.com/in/',
      },
    },
  ];

</script>

<style>
  .grid {
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

<div class="grid">
  {#each teamMembers as member}
    <TeamCard
      name={member.name}
      position={member.position}
      description={member.description}
      imageUrl={member.imageUrl}
      socialLinks={member.socialLinks}
    />
  {/each}
</div>
