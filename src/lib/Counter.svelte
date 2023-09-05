<script>
	let count = 0;
	$: string = `You have clicked ${count} times`;

	$: if (count >= 10) {
		alert(`count is dangerously high!`);
		count = 9;
	}

	function increment() {
		count += 1;
	}
</script>

<button on:click={increment}>clicks {count}</button>
<p>{string}</p>

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
