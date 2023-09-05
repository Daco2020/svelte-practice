<script>
	let count1 = 0;
	let count2 = 0;
	let count3 = 0;

	function setCount3(x) {
		count3 = x * 2;
		return count3;
	}
	function getTotal(x, y) {
		return x + y;
	}

	$: string1 = `You have clicked ${getTotal(count1, count2)} times`;

	// 변경 순서가 보장되어야 정상 동작한다.
	$: setCount3(count1);
	$: string3 = `Count3 is ${count3}`;

	function increment1() {
		count1 += 1;
	}
	function increment2() {
		count2 += 1;
	}
</script>

<button on:click={increment1}>clicks {count1}</button>
<button on:click={increment2}>clicks {count2}</button>

<p>{string1}</p>
<p>{string3}</p>

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
