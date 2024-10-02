<script>
	import TeamCard from '../components/TeamCard.svelte';
	import TeamGrid from '../components/TeamGrid.svelte';
	import { TableRonde } from '../data/TableRonde.js';
	import { LaCours } from '../data/LaCours.js';
</script>

<div>
  <h1>Notre equipe</h1>
  <h2>La table ronde</h2>
  <TeamGrid class="membres" members={TableRonde} />
  <h2>La cours</h2>
  <TeamGrid members={LaCours} />
</div>

<style>
  * {
    font-family: 'Poppins', sans-serif;
  }
  h1 {
    text-align: center;
    font-family: 'Cyberion';
    font-weight: normal;
    font-style: normal;
    color: var(--text-highlight);
  }

  h2 {
    font-family: 'Cyberion';
    font-weight: normal;
    font-style: normal;

    text-align: center;
  }
  membres {
    font-family: 'Poppins';
  }
</style>
