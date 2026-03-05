<script lang="ts">
	import './layout.css';
	import favicon from '$lib/assets/favicon.svg';
	import { ModeWatcher } from 'mode-watcher';
	import * as Sidebar from '$lib/components/ui/sidebar/index';
	import AppSidebar from '$lib/components/app-sidebar.svelte';
	import AppHeader from '$lib/components/app-header.svelte';
	import AppThemeToggler from '$lib/components/app-theme-toggler.svelte';
	let { children } = $props();
</script>

<svelte:head><link rel="icon" href={favicon} /></svelte:head>

<ModeWatcher />

<Sidebar.Provider>
	<AppThemeToggler />
	<AppSidebar />
	<main class="flex h-screen w-full flex-col">
		<AppHeader />
		<section class="flex-1">
			{@render children()}
		</section>
	</main>
</Sidebar.Provider>
