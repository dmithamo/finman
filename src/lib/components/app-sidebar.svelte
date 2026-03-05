<script lang="ts">
	import * as Sidebar from '$lib/components/ui/sidebar/index';
	import AppLogo from './app-logo.svelte';

	import { useSidebar } from '$lib/components/ui/sidebar/index';
	import AppThemeToggler from './app-theme-toggler.svelte';
	const sidebar = useSidebar();

	const user = {
		fullname: 'D Mithamo',
		email: 'b@dmithamo.dev'
	};
</script>

<Sidebar.Root collapsible="icon">
	<Sidebar.Header class="p-5">
		<a class="w-fit" href="/">
			<AppLogo isFull={sidebar.state === 'expanded'} />
		</a>
	</Sidebar.Header>
	<Sidebar.Content />
	<Sidebar.Footer>
		<Sidebar.Trigger />
	</Sidebar.Footer>
</Sidebar.Root>
