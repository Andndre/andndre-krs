<script lang="ts">
	import * as icons from 'lucide-svelte';
	// @ts-ignore
	export let name: string;
	export let className: string | undefined = undefined;
	// @ts-ignore
	let icon = icons[name];
</script>

<svelte:component class={className} this={icon} {...$$props} />
