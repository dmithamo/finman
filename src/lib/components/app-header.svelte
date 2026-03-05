<script lang="ts">
	import type { Component } from 'svelte';
	import { BookOpenText, BellRing, type IconProps } from '@lucide/svelte';

	const hLinks: Array<{
		href: string;
		label: string;
		icon: Component<IconProps>;
	}> = [
		{
			href: '/guides',
			label: 'Guides',
			icon: BookOpenText
		},

		{
			href: '/notifications',
			label: 'Notifications',
			icon: BellRing
		}
	];
</script>

<header class="flex h-16 w-full items-center justify-end gap-8 border-b px-8 text-sm">
	{#each hLinks as link (link.href)}
		{@render headerLink(link)}
	{/each}
</header>

{#snippet headerLink(link: (typeof hLinks)[0])}
	<a title={link.label} class="flex items-center gap-4 text-xs hover:text-chart-2" href={link.href}>
		<link.icon class="h-[1.2rem] w-[1.2rem]" />
	</a>
{/snippet}
