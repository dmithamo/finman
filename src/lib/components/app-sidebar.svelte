<script lang="ts">
	import * as Sidebar from '$lib/components/ui/sidebar/index';
	import AppLogo from './app-logo.svelte';

	import { useSidebar } from '$lib/components/ui/sidebar/index';
	const sidebar = useSidebar();

	const user = {
		fullname: 'D Mithamo',
		email: 'b@dmithamo.dev'
	};
</script>

<Sidebar.Root collapsible="icon">
	<Sidebar.Header class="p-5">
		<AppLogo isFull={sidebar.state === 'expanded'} />
	</Sidebar.Header>
	<Sidebar.Content />
	<Sidebar.Footer>
		<Sidebar.Trigger />
	</Sidebar.Footer>
</Sidebar.Root>
