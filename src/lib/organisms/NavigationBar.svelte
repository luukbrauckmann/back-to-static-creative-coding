<script>
	import NavItem from '$lib/molecules/NavItem.svelte';

	let items = [
		{ icon: 'home', label: 'Home', href: '/' },
		{ icon: 'players', label: 'Players', href: '/' },
		{ icon: 'teams', label: 'Teams', href: '/' },
		{ icon: 'tournaments', label: 'Tournaments', href: '/' },
		{ icon: 'live', label: 'Live', href: '/' }
	];
</script>

<nav aria-label="Main Navigation">
	<ul>
		{#each items as item}
			<NavItem {item} />
		{/each}
	</ul>
</nav>

<style>
	nav {
		padding: 0.5em;
		height: 100%;
	}

	ul {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		gap: 4rem;
		box-shadow: var(--box-shadow);
		border-radius: 10px;
		background-color: var(--input-background-color);
		height: 100%;
		list-style: none;
	}
</style>
