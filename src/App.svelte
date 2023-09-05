<script>
	import Counter from './lib/Counter.svelte';

	const props = {
		maxCount: 10,
		initialCount: 3,
		restProps: 'foo'
	};
</script>

<!-- 두 컴포넌트는 동일 -->
<Counter initialCount={props.initialCount} maxCount={props.maxCount} />
<Counter {...props} />

<style>
</style>
