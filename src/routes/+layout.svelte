<body>
	<nav>
		<div class="logo">
			<a href="/">danijel jerinic</a>
		</div>
		<ul>
			<li><a href="/about" class="nav-link">About</a></li>
			<li><a href="/cv" class="nav-link">CV</a></li>
		</ul>
		<ul class="big-screen-list">
			<p>WEB INTERFACE</p>
			<li>eVenue</li>
			<li>Stock</li>
			<li>Ordermatch</li>
		</ul>
		<ul class="big-screen-list">
			<p>CONTACT</p>
			<li>Mail</li>
			<li>Twitter</li>
			<li>LinkedIn</li>
		</ul>
	</nav>
	<slot></slot>
</body>

<style>
	* {
		padding: 0;
		margin: 0;

		box-sizing: border-box;

		font-family:
			system-ui,
			-apple-system,
			BlinkMacSystemFont,
			'Segoe UI',
			Roboto,
			Oxygen,
			Ubuntu,
			Cantarell,
			'Open Sans',
			'Helvetica Neue',
			sans-serif;
	}

	.logo {
		height: max-content;
		width: max-content;
		padding: 4px;

		border-radius: 5px;

		background-color: #f3f2f2;
	}

	.logo a {
		text-decoration: none;

		color: #3b3d41;

		font-weight: 600;
		font-size: 20px;
	}

	@media screen and (max-width: 809.98px) {
		nav {
			position: fixed;

			display: flex;
			justify-content: space-between;
			align-items: center;

			top: 0;
			left: 0;

			height: max-content;
			padding: 16px;
			width: 100%;

			z-index: 9999;

			background-color: rgba(255, 255, 255, 0.75);
		}

		nav ul {
			list-style-type: none;

			display: flex;
			gap: 16px;
		}

		nav ul li {
			font-size: 20px;
			font-weight: 500;
			color: #3b3d41;
			letter-spacing: -0.025rem;
		}

		.big-screen-list {
			display: none;
		}
	}

	nav ul li .nav-link {
		height: max-content;
		width: max-content;
		text-decoration: none;
		color: inherit;
		display: contents;
	}

	@media screen and (min-width: 809.99px) {
		nav {
			position: fixed;
			top: 0;
			left: 0;

			padding: 40px 0;

			height: 100%;
			width: 184px;

			border-right: 1px solid #dcdcdc;

			display: flex;
			flex-direction: column;
			justify-content: flex-start;
			align-items: flex-start;
		}

		.logo {
			margin-left: 16px;
		}

		nav ul {
			width: 100%;

			padding: 16px 16px 24px 16px;

			list-style-type: none;
			display: flex;
			flex-direction: column;
			gap: 8px;
			border-bottom: 1px solid #dcdcdc;
		}

		nav ul li {
			font-size: 20px;
			font-weight: 500;
			color: #3b3d41;
			letter-spacing: -0.025rem;
		}

		.big-screen-list {
			height: max-content;
			width: 100%;

			padding: 24px 16px;

			border-bottom: 1px solid #dcdcdc;
		}

		.big-screen-list p {
			font-size: 14px;
			letter-spacing: 0.1rem;
			color: #a2a2a2;
		}

		.big-screen-list li {
			font-weight: normal;
			font-size: 14px;
		}

		.big-screen-list:last-child {
			border-bottom: none;
		}
	}
</style>
