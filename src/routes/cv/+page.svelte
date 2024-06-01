<script>
	import CVBlock from '../../components/CVBlock.svelte';
</script>

<div class="wrapper">
	<CVBlock />
</div>

<style>
	.wrapper {
		position: fixed;
		top: 0;
		left: 0;

		padding-top: 48px;

		height: 100%;
		width: calc(100% - 184px);

		margin-left: 184px;

		display: flex;
		flex-direction: column;
		justify-content: flex-start;
		align-items: center;
	}

	@media screen and (max-width: 809.98px) {
		.wrapper {
			position: relative;

			width: 100%;

			display: flex;
			flex-direction: column;
			justify-content: center;
			align-items: center;

			margin-left: 0;
		}
	}
</style>
