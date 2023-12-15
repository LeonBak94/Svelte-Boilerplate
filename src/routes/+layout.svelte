<script lang="ts">
	import '../app.css';
	import Navbar from './layout/Navbar.svelte';
	import Sidebar from './layout/Sidebar/Sidebar.svelte';
	// import Error from './error/+page.svelte'

	import { page } from '$app/stores';
</script>

<svelte:head>
	<title>SvelteKit</title>
	<meta name="description" content="SvelteKit Template" />
	<link rel="icon" href="%sveltekit.assets%/favicon.png" />
</svelte:head>

<svelte>
	<div class="flex w-full flex-col h-screen">
		<Navbar />
		<div class="flex w-full flex-1">
			<Sidebar />
			{#if $page.status!=404}
				<slot />
				{:else}
					<!-- <Error /> -->
			{/if}		
		</div>
	</div>
</svelte>
