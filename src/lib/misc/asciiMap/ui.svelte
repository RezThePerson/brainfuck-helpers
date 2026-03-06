<script>
	import map from './map.json';
	import Cell from './cell.svelte';
</script>

<div class="m-3 flex flex-col gap-2 border-3 border-neutral-400 p-3">
	<h1 class="text-4xl" id="ascii-map">ascii map</h1>

	<div>
		<div class="flex w-full gap-4">
			<span class="w-1/8 border-2 border-neutral-900 text-neutral-600"> decimal </span>
			<span class="w-1/8 border-2 border-neutral-900 text-neutral-600"> hexadecimal </span>
			<span class="w-2/8 border-2 border-neutral-900 text-neutral-600"> character </span>

			<span class="w-4/8 border-2 border-neutral-900 text-neutral-600"> description </span>
		</div>

		<div class="flex flex-col gap-2">
			{#each map as cell (cell.dec)}
				<Cell
					decimal={cell.dec}
					hex={'0x' + cell.dec.toString(16).padStart(2, '0').toUpperCase()}
					char={cell.char}
					desc={cell.desc}
				/>
			{/each}
		</div>
	</div>
</div>
