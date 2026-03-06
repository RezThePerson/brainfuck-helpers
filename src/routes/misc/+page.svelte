<script>
	import { resolve } from '$app/paths';

	import CharMultiplierUi from '$lib/misc/charMultiplier/ui.svelte';
	import AsciiMapUi from '$lib/misc/asciiMap/ui.svelte';
</script>

<div class="flex flex-col">
	<div class="m-3 flex flex-col gap-2 border-3 border-neutral-900 p-3">
		<h1 class="text-6xl">misc brainfuck stuff</h1>

		<div class="flex gap-5">
			<a href={resolve('/')} class="text-blue-600 dark:text-blue-400">go back</a>
			<a href="#char-multiplier" class="text-blue-600 dark:text-blue-400">char multiplier</a>
			<a href="#ascii-map" class="text-blue-600 dark:text-blue-400">ascii map</a>
		</div>
	</div>

	<CharMultiplierUi />
	<AsciiMapUi />
</div>
