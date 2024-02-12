<script>
  import AppFooter from "$lib/components/my/AppFooter.svelte";
	import AppHeader from "$lib/components/my/AppHeader.svelte";
	import { ModeWatcher } from "mode-watcher";
	import "../app.css";
</script>

<ModeWatcher />

<div class="bg-white dark:bg-gray-900">
	<AppHeader/>
		<slot />
	<AppFooter/>
</div>
