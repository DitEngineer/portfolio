<div class="box">
	<p class="heading">CRAFT</p>
	<slot></slot>
	<div class="description">
		<div class="info">
			<p class="project-name">eVenue</p>
			<p class="project-part">Design and Development</p>
		</div>
		<p class="time-span">2024-</p>
	</div>
</div>

<style>
	* {
		padding: 0;
		margin: 0;
		box-sizing: border-box;
	}

	.description {
		height: max-content;
		width: 100%;

		display: flex;
		justify-content: space-between;
	}

	.project-name,
	.project-part {
		font-size: 22px;
		letter-spacing: -0.025rem;
	}

	.project-name {
		color: #3b3d41;
	}

	.project-part {
		font-weight: 500;
		color: #a2a2a2;
	}

	.time-span {
		font-size: 14px;
		color: #a2a2a2;
		font-weight: 400;
	}

	@media screen and (max-width: 809.99px) {
		.box {
			border-top: 1px solid #dcdcdc;

			height: max-content;
			padding: 8px 0;

			font-weight: 500;
			font-size: 12px;
			letter-spacing: 0.1rem;
			color: #a2a2a2;

			display: flex;
			flex-direction: column;
			gap: 16px;
		}

		.project-name,
		.project-part {
			font-size: 22px;
			letter-spacing: -0.025rem;
		}

		.project-name {
			color: #3b3d41;
		}

		.project-part {
			font-weight: 500;
		}

		.time-span {
			font-size: 14px;
			color: #a2a2a2;
			font-weight: 400;
		}
	}

	@media screen and (min-width: 810px) {
		.box {
			border-top: 1px solid #dcdcdc;

			padding: 8px 0;

			display: flex;
			flex-direction: column;
			gap: 24px;
		}
	}
</style>
