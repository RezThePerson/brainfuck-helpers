<script>
	import './layout.css';
	import favicon from '$lib/assets/favicon.svg';

	let { children } = $props();
</script>

<svelte:head><link rel="icon" href={favicon} /></svelte:head>

<div class="h-screen p-5 dark:bg-neutral-900 dark:text-white">
	<div class="h-full overflow-scroll border-3 border-black p-5 dark:border-white">
		{@render children()}
	</div>
</div>
