<script lang="ts">
	import codeStyle from "svelte-highlight/styles/github";
	import Hero from './Hero.svelte';
	import AboutMe from './AboutMe.svelte';
	import Techs from './Techs.svelte';
	import Projects from './Projects.svelte';

</script>

<svelte:head>
  {@html codeStyle}

	<style>
		.code-wrapper div {
			border-radius: 1rem;
			overflow: hidden;
			border: 1px gray solid;
		}
	</style>	
</svelte:head>
<Hero/>
<div class="pt-16"></div>
<AboutMe/>
<div class="pt-16"></div>
<Projects/>
<div class="pt-16"></div>
<Techs/>
