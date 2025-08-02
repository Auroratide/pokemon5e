<script lang="ts">
	import type { Snippet } from "svelte"

	let {
		title,
		children,
	}: {
		title: string,
		children: Snippet,
	} = $props()
</script>

<svelte:head>
	<title>{title}</title>
</svelte:head>

<main>
	<div class="container">
		<header>
			<h1>{title}</h1>
		</header>
		{@render children()}
	</div>
</main>

<style>
	main {
		text-align: center;
		margin-block: 4em;
	}

	header {
		margin-block-end: 2em;
	}

	h1 {
		font-weight: bold;
	}

	.container {
		max-inline-size: 37.5rem;
		margin: auto;
	}
</style>
