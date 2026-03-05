<script lang="ts">
	import logoSvg from '$lib/assets/favicon.svg?raw';
	let { isFull } = $props();
</script>

<div class="flex items-center">
	<span class="text-green-500">
		{@html logoSvg}
	</span>
	{#if isFull}
		<span
			class="ml-2 flex items-center bg-linear-to-r from-green-500 to-orange-400 bg-clip-text font-mono text-lg font-bold text-transparent"
		>
			fintra
		</span>
	{/if}
</div>
