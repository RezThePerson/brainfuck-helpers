<script>
	let props = $props();
</script>

<div class="flex w-full gap-4">
	<button
		class="w-1/8 cursor-pointer border-2 border-neutral-600 px-2 py-1 text-left hover:border-blue-600"
		onclick={(e) => {
			e.target.innerText = 'copied!';
			navigator.clipboard.writeText(props.decimal);
			setTimeout(() => (e.target.innerText = props.decimal), 500);
		}}
	>
		{props.decimal}
	</button>
	<button
		class="w-1/8 cursor-pointer border-2 border-neutral-600 px-2 py-1 text-left hover:border-blue-600"
		onclick={(e) => {
			e.target.innerText = 'copied!';
			navigator.clipboard.writeText(props.hex);
			setTimeout(() => (e.target.innerText = props.hex), 500);
		}}
	>
		{props.hex}
	</button>
	<button
		class="w-2/8 cursor-pointer border-2 border-neutral-600 px-2 py-1 text-left hover:border-blue-600"
		onclick={(e) => {
			e.target.innerText = 'copied!';
			navigator.clipboard.writeText(props.char);
			setTimeout(() => (e.target.innerText = props.char), 500);
		}}
	>
		{props.char}
	</button>
	<span class="w-4/8 border-2 border-neutral-600 px-2 py-1">
		{props.desc}
	</span>
</div>
