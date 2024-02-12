<script>
  import AppFooter from "$lib/components/my/AppFooter.svelte";
	import AppHeader from "$lib/components/my/AppHeader.svelte";
	import "../app.css";
</script>

<div class="bg-white dark:bg-gray-900">
	<AppHeader/>
		<slot />
	<AppFooter/>
</div>
