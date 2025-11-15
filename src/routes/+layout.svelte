<script lang="ts">
	import "../app.css";
	import favicon from "$lib/assets/favicon.svg";

	let { children } = $props();
</script>

<svelte:head>
	<link
		rel="icon"
		href={"https://i.pinimg.com/736x/00/17/41/0017417cdb2476a3fb0380e2c8d0a347.jpg"}
	/>
	<title>le buba | portfolio</title>
</svelte:head>

{@render children()}
