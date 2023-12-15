<script lang="ts">
	import '../app.css';
	import Navbar from './layout/Navbar.svelte';
	import Sidebar from './layout/Sidebar/Sidebar.svelte';
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
			<div class="content">
				<slot />
			</div>
		</div>
	</div>
</svelte>
