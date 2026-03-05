<script lang="ts">
	import logoSvg from '$lib/assets/favicon.svg?raw';
	let { isFull = true, isNameOnly = false } = $props();
	const APP_NAME = 'finatra';
</script>

{#if !isNameOnly}
	<div class="flex items-center">
		<span class="text-chart-2">
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
	<span class="text-gradient">
		{APP_NAME}
	</span>
{/snippet}
