<script>
	import { name } from "./Stores/stores.js";
	import Info from "./Modals/Info.svelte";
	let infoScreen = true;
</script>

<main>
	<h1>Hello {$name}</h1>
	{#if infoScreen}
		<Info on:close="{() => infoScreen = false}"/>
	{/if}
</main>

<style>
</style>