<script>
	let characterToMultiply = $state('');
	let timesToMultiply = $state(0);

	let copied = $state(false);
</script>

<div class="m-3 flex flex-col gap-2 border-3 border-neutral-400 p-3">
	<h1 class="text-4xl" id="char-multiplier">char multiplier</h1>

	<div class="flex w-full gap-4">
		<div class="flex w-1/2 flex-col-reverse">
			<input
				type="text"
				class="peer w-full border-2 border-neutral-600 px-2 py-1 focus:border-blue-600 focus:outline-none"
				bind:value={characterToMultiply}
			/>
			<span class="border-2 border-neutral-900 text-neutral-600 peer-focus:text-blue-600">
				character to multiply:
			</span>
		</div>
		<div class="flex w-1/2 flex-col-reverse">
			<input
				type="text"
				class="peer w-full border-2 border-neutral-600 px-2 py-1 focus:border-blue-600 focus:outline-none"
				bind:value={timesToMultiply}
			/>
			<span class="border-2 border-neutral-900 text-neutral-600 peer-focus:text-blue-600">
				no of times to multiply:
			</span>
		</div>
	</div>
	<div class="flex w-full gap-4">
		<input
			type="text"
			placeholder="output"
			readonly
			class="w-full border-2 border-neutral-600 px-2 py-1 focus:border-blue-600 focus:outline-none"
			value={characterToMultiply.repeat(timesToMultiply)}
		/>
		<button
			class="w-1/4 cursor-pointer border-2 border-neutral-600 px-2 py-1 hover:border-blue-600"
			onclick={() => {
				copied = true;
				navigator.clipboard.writeText(characterToMultiply.repeat(timesToMultiply));
				setTimeout(() => (copied = false), 500);
			}}
		>
			{copied ? 'copied!' : 'copy'}
		</button>
	</div>
</div>
