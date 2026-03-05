<script lang="ts">
	import logoSvg from '$lib/assets/favicon.svg?raw';
	let { isFull = true, isNameOnly = false } = $props();
	const APP_NAME = 'finatra';
</script>

{#if !isNameOnly}
	<div class="flex items-center">
		<span class="text-green-500">
			{@html logoSvg}
		</span>
		{#if isFull}
			<span class="ml-2 flex items-center text-lg">
				{@render appName()}
			</span>
		{/if}
	</div>
{/if}

{#if isNameOnly}
	{@render appName()}
{/if}

{#snippet appName()}
	<span
		class="bg-linear-to-r from-green-500 to-orange-400 bg-clip-text font-mono font-bold text-transparent"
	>
		{APP_NAME}
	</span>
{/snippet}
