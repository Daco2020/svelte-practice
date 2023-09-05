<script>
	export let initialCount;
	export let maxCount;

	console.log($$props, $$restProps);

	// $$props
	// {
	//   "maxCount": 10,
	//   "initialCount": 3,
	//   "restProps": "foo"
	// }

	// $$restProps
	// {
	//   "restProps": "foo"
	// }

	let count = initialCount;

	function increment() {
		if (count >= maxCount) return;
		count += 1;
	}
</script>

<button on:click={increment}>clicks {count}</button>

<style>
	button {
		font-size: 1em;
		padding: 0.5em 1em;
		color: #fff;
		background-color: #ff3e00;
		border: none;
		border-radius: 3px;
		cursor: pointer;
	}
</style>
