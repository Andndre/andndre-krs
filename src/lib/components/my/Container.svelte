<script lang="ts">
	import { cn } from "$lib/utils";
import type { HTMLHtmlAttributes } from "svelte/elements";

let className: HTMLHtmlAttributes['class'] = undefined;
export { className as class };
</script>

<div class={cn("max-w-7xl mx-auto px-6 md:px-12 xl:px-6", className)}>
	<slot />
</div>
