<script>
	export let size = 'small';
	export let shadow = false;
</script>

<button class:size-lg={size === 'large'} class:size-sm={size === 'small'} class:shadow>
	<slot>Default Button</slot>
</button>

<style lang="scss">
	button {
		background-color: #4caf50;
		border: none;
		color: white;
		cursor: pointer;
		&:hover {
			background-image: linear-gradient(rgba(0, 0, 0, 0.1) 0 0);
		}
		&:active {
			background-image: linear-gradient(rgba(255, 255, 255, 0.1) 0 0);
		}
		&.size-sm {
			padding: 15px 20px;
		}
		&.size-lg {
			padding: 20px 25px;
			font-size: 20px;
		}
		&.shadow {
			box-shadow: 0px 3px 5px rgba(0, 0, 0, 0.3);
		}
	}
</style>
