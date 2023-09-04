<script>
	let name = 'Svelte';
	let src =
		'https://i.namu.wiki/i/U8nWyvc76Ps3GJsJGKBvDzxh1HWD0WSgncBDKNvHskPmGS5rOjxBy864oRb2gEtGeRWolxY6p99R6IEaShbSqQ.webp';
	let string = 'Some <strong>string</strong> with html';
</script>

<img {src} alt="Sume text {name}" />
<h1>Hello {name.toUpperCase()}!</h1>
<p>{@html string}</p>

<style>
	h1 {
		color: red;
	}
</style>
