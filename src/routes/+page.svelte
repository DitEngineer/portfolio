<script>
	import CraftBox from '../components/CraftBox.svelte';
	import ProjectFrame from '../components/ProjectFrame.svelte';
</script>

<div class="wrapper">
	<p class="greet">Hello world!</p>
	<h1 class="intro-text">
		Danijel is a designer crafting interfaces that are useful and simple to use. He loves creating
		useful solutions out of complex problems. He's a junior front end developer at CloverLabs,
		Maribor - Slovenia.
	</h1>

	<CraftBox>
		<ProjectFrame />
	</CraftBox>

	<footer>
		<p>EC. 2024</p>
		<ul class="socials">
			<li>Instagram</li>
			<li>Twitter</li>
			<li>LinkedIn</li>
		</ul>
	</footer>
</div>

<style>
	* {
		padding: 0;
		margin: 0;

		box-sizing: border-box;
	}

	.wrapper {
		height: 100vh;
		width: 100%;

		background-color: #fefefe;
	}

	.greet {
		font-size: 20px;
		font-weight: 500;
		background: linear-gradient(to right, #a2a2a2, #3b3d41);
		background-clip: text;
		color: transparent;
	}

	.intro-text {
		font-weight: 500;
		letter-spacing: -0.025rem;

		background: linear-gradient(to right, #a2a2a2, #3b3d41);
		background-clip: text;
		color: transparent;

		margin-bottom: 12px;
	}

	@media screen and (max-width: 809.99px) {
		.wrapper {
			margin-top: 72px;

			display: flex;
			flex-direction: column;
			gap: 24px;

			padding: 16px;
		}

		.intro-text {
			font-size: 22px;
		}

		footer {
			margin: 0 -16px;

			height: max-content;
			padding: 24px 16px;
			width: calc(100% + 32px);

			display: flex;
			justify-content: space-between;
			align-items: center;

			border-top: 1px solid #dcdcdc;
		}

		footer p {
			font-size: 14px;
			color: #3b3d41;
			font-weight: 500;
		}

		footer .socials {
			height: max-content;
			width: max-content;

			list-style-type: none;

			display: flex;
			gap: 12px;
		}

		footer .socials li {
			font-size: 14px;
			color: #3b3d41;
		}
	}

	@media screen and (min-width: 810px) {
		.wrapper {
			position: fixed;
			left: 184px;
			top: 0;

			height: 100%;
			width: calc(100% - 184px);

			padding: 48px 40px 0px 40px;

			display: flex;
			flex-direction: column;
			gap: 24px;

			overflow: auto;
		}

		.intro-text {
			font-size: 40px;
			letter-spacing: -0.1rem;
		}

		footer {
			height: max-content;
			padding: 24px 16px;
			width: calc(100% + 80px);

			margin: 0 -40px;

			display: flex;
			justify-content: space-between;
			align-items: center;

			border-top: 1px solid #dcdcdc;
		}

		footer .socials {
			height: max-content;
			width: max-content;

			list-style-type: none;

			display: flex;
			gap: 12px;
		}
	}
</style>
