<script>
	import TeamCard from '../components/TeamCard.svelte';
	import TeamGrid from '../components/TeamGrid.svelte';
	import { TableRonde } from '../data/TableRonde.js';
	import { LaCours } from '../data/LaCours.js';
</script>

<div>
	<h1>Notre équipe</h1>
	<h2>La table ronde</h2>
	<TeamGrid members={TableRonde} />
	<h2>La cours</h2>
	<TeamGrid members={LaCours} />
</div>

<style>
	h1 {
		text-align: center;
	}

	h2 {
		text-align: center;
		color: #2d3748;
	}
</style>
