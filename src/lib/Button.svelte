<script>
</script>

<button><slot /></button>
<button> <slot>Default Button</slot></button>

<style lang="scss">
	button {
		background-color: #4caf50;
		border: none;
		color: white;
		padding: 16px 16px;
		font-size: 16px;
		cursor: pointer;
		&:hover {
			background-color: variables.$color;
		}
	}
</style>
